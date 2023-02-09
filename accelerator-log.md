# Accelerator Log

## Options
```json
{
  "bsGitBranch" : "main",
  "bsGitRepository" : "github.com?owner=garethjevans&repo=library-supply-chain",
  "buildTool" : "kpack",
  "configWriterTemplate" : "config-writer-and-pull-requester-template",
  "externalDeliveryTemplate" : "deliverable-template",
  "hasImageScan" : false,
  "hasSourceScan" : true,
  "hasTests" : true,
  "imageScanningTool" : "grype",
  "projectName" : "library-supply-chain",
  "sourceScanningTool" : "grype",
  "workloadType" : "library"
}
```
## Log
```
┏ engine (Chain)
┃  Info Running Chain(GeneratorValidationTransform, UniquePath)
┃ ┏ ┏ engine.transformations[0].validated (Combo)
┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ engine.transformations[0].validated.delegate (Chain)
┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃  Info Running Merge(Combo, Combo)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[0].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, Exclude)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[0].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**]
┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug Makefile matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug README.md matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug build-local.sh matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/all-options.json matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/default-options.json matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/expected-all-options.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┗ Debug tests/expected-default-options.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[0].delegate.transformations[1] (Exclude)
┃ ┃ ┃ ┃ ┃ ┃  Info Will exclude [Makefile, build-local.sh, generated/**, tests/**]
┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug Makefile matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug build-local.sh matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml didn't match [Makefile, build-local.sh, generated/**, tests/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/all-options.json matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/default-options.json matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/expected-all-options.yaml matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┗ ┗ Debug tests/expected-default-options.yaml matched [Makefile, build-local.sh, generated/**, tests/**] -> excluded
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, Combo, Combo, Combo, Combo, Combo, Combo, Combo, Combo, Combo)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃  Info Will include [README.md, config/*.yaml]
┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug Makefile didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug README.md matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug build-local.sh didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/all-options.json didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/default-options.json didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ Debug tests/expected-all-options.yaml didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┗ Debug tests/expected-default-options.yaml didn't match [README.md, config/*.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [configWriterTemplate->config-writer-and-pu...(truncated), buildTool->kpack-template, source-test-scan-to-url->library-supply-chain, externalDeliveryTemplate->deliverable-template, workloadType->library]
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2] (Combo)
┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(InvokeFragment, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0] (InvokeFragment)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0].validated (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#bsGitRepository != null) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Let
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0].validated.delegate (Let)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Adding symbol repoUrl with value 'https://github.com?owner=garethjevans&repo=library-supply-chain'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0].validated.delegate.in (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(OpenRewriteRecipe, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ╺ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0].validated.delegate.in.transformations[0] (OpenRewriteRecipe)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[0].validated.delegate.in.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ ┗ ┗  Info Will replace regex '(?<beforeBranch>[\s\S]+)(?<branch>branch: [\S]+)(?<rest>[\S\s]*)' with '${beforeBranch}branc...(truncated)'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Include
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[0].sources[1].delegate (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug config/values.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[2].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/values.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/cluster-supply-chain.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/schema.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug Multiple representations for path 'README.md', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[3] (Combo)
┃ ┃ ┃ ┃ ┃ ┗  Info Condition (!#hasTests) evaluated to false
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[4] (Combo)
┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#hasTests) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[4].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[4].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [README.md, config/*.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug README.md matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[4].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace regex '# StartNoTests[\s\S]+?# EndNoTests' with ''
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[4].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗ ┗  Info Will replace regex '# StartTests\s|# EndTests\s' with ''
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[5] (Combo)
┃ ┃ ┃ ┃ ┃ ┗  Info Condition (!#hasSourceScan) evaluated to false
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[6] (Combo)
┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#hasSourceScan) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[6].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[6].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [README.md, config/*.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug README.md matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[6].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace regex '# StartNoSourceScan[\s\S]+?# EndNoSourceScan\s' with ''
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[6].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗ ┗  Info Will replace regex '# StartSourceScan\s|# EndSourceScan\s' with ''
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[7] (Combo)
┃ ┃ ┃ ┃ ┃ ┃  Info Condition (!#hasImageScan) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[7].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[7].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [README.md, config/*.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug README.md matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[7].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace regex '# StartImageScan[\s\S]+?# EndImageScan' with ''
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[7].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┗ ┗  Info Will replace regex '# StartNoImageScan\s|# EndNoImageScan\s' with ''
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[8] (Combo)
┃ ┃ ┃ ┃ ┃ ┗  Info Condition (#hasImageScan) evaluated to false
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[9] (Combo)
┃ ┃ ┃ ┃ ┃ ┗  Info Condition (#configWriterTemplate == 'config-writer-template') evaluated to false
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[10] (Combo)
┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#configWriterTemplate != 'config-writer-template') evaluated to true
┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[10].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[10].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [README.md, config/*.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/values.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/cluster-supply-chain.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/schema.yaml matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug README.md matched [README.md, config/*.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[10].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace regex '# StartNoGitOps[\s\S]+?# EndNoGitOps\s' with ''
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[0].sources[1].delegate.transformations[10].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┗ ┗ ┗ ┗  Info Will replace regex '# StartGitOps\s|# EndGitOps\s' with ''
┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/values.yaml', will use the one appearing last 
┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/cluster-supply-chain.yaml', will use the one appearing last 
┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/schema.yaml', will use the one appearing last 
┃ ┗ ┗ ┗ Debug Multiple representations for path 'README.md', will use the one appearing last 
┗ ╺ engine.transformations[1] (UniquePath)
```
