# Cognitive Services Video Search SDK

> see https://aka.ms/autorest

Configuration for generating Video Search SDK.

The current release is `release_1_0`.

``` yaml

tag: release_1_0
add-credentials: true
openapi-type: data-plane
```
# Releases

### Release 1.0
These settings apply only when `--tag=release_1_0` is specified on the command line.

``` yaml $(tag) == 'release_1_0'
input-file: v1.0/VideoSearch.json
```

## CSharp Settings
These settings apply only when `--csharp` is specified on the command line.
``` yaml $(csharp)
csharp:
  namespace: Microsoft.Azure.CognitiveServices.Search.VideoSearch
  output-folder: $(csharp-sdks-folder)/CognitiveServices/dataPlane/Search/BingVideoSearch/BingVideoSearch/Generated/VideoSearch
  sync-methods: none
```

## Python

These settings apply only when `--python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.
Use `--python-mode=update` if you already have a setup.py and just want to update the code itself.

``` yaml $(python)
python-mode: create
python:
  license-header: MICROSOFT_MIT_NO_VERSION
  add-credentials: true
  payload-flattening-threshold: 2
  namespace: azure.cognitiveservices.search.videosearch
  package-name: azure-cognitiveservices-search-videosearch
  clear-output-folder: true
```
``` yaml $(python) && $(python-mode) == 'update'
python:
  no-namespace-folders: true
  output-folder: $(python-sdks-folder)/azure-cognitiveservices-search-videosearch/azure/cognitiveservices/search/videosearch
```
``` yaml $(python) && $(python-mode) == 'create'
python:
  basic-setup-py: true
  output-folder: $(python-sdks-folder)/azure-cognitiveservices-search-videosearch
```

## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: videosearch
  clear-output-folder: true
```

### Tag: release_1_0 and go

These settings apply only when `--tag=release_1_0 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'release_1_0' && $(go)
output-folder: $(go-sdk-folder)/services/cognitiveservices/v1.0/videosearch
```