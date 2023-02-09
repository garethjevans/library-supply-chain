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
kapp -y deploy -a library-supply-chain -f <(ytt -f ./config)
```
