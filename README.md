# library-supply-chain

## Installation

To install this into a cluster use:

```
ytt \
  --ignore-unknown-comments \
  --file ./config \
  --data-values-file values.yaml |
  kubectl apply -f-
```

Or with `kapp`

```
kapp -y deploy -a library-supply-chain -f <(ytt -f ./config --data-values-file values.yaml)
```

## Configure a workload

```
tanzu apps workload create go-scm \
  --git-branch main \
  --git-repo https://github.com/jenkins-x/go-scm \
  --namespace dev \
  --label app.kubernetes.io/part-of=go-scm \
  --param-yaml testing_pipeline_matching_labels='{"apps.tanzu.vmware.com/pipeline":"golang-pipeline"}' \
  --param-yaml testing_pipeline_params='{}' \
  --type library \
  --yes
```

## Golang Pipeline

```
apiVersion: tekton.dev/v1beta1
kind: Pipeline
metadata:
  labels:
    apps.tanzu.vmware.com/pipeline: golang-pipeline
  name: developer-defined-golang-pipeline
  namespace: dev
spec:
  params:
  - name: source-url
    type: string
  - name: source-revision
    type: string
  tasks:
  - name: test
    params:
    - name: source-url
      value: $(params.source-url)
    - name: source-revision
      value: $(params.source-revision)
    taskSpec:
      metadata: {}
      params:
      - name: source-url
        type: string
      - name: source-revision
        type: string
      steps:
      - image: golang
        name: test
        resources: {}
        script: |
          cd `mktemp -d`
          wget -qO- $(params.source-url) | tar xvz -m
          go test ./...
```
