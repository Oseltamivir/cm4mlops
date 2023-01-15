*This README is automatically generated - don't edit! Use `README-extra.md` for extra notes!*

<details>
<summary>Click here to see the table of contents.</summary>

* [About](#about)
* [Category](#category)
* [Origin](#origin)
* [Meta description](#meta-description)
* [Tags](#tags)
* [Variations](#variations)
  * [ All variations](#all-variations)
* [Versions](#versions)
* [Default environment](#default-environment)
* [CM script workflow](#cm-script-workflow)
* [New environment export](#new-environment-export)
* [New environment detected from customize](#new-environment-detected-from-customize)
* [Usage](#usage)
  * [ CM installation](#cm-installation)
  * [ CM script automation help](#cm-script-automation-help)
  * [ CM CLI](#cm-cli)
  * [ CM Python API](#cm-python-api)
  * [ CM modular Docker container](#cm-modular-docker-container)
* [Maintainers](#maintainers)

</details>

___
### About

*TBD*
___
### Category

Modular MLPerf benchmarks.
___
### Origin

* GitHub repository: *[mlcommons@ck](https://github.com/mlcommons/ck/tree/master/cm-mlops)*
* CM artifact for this script (interoperability module, native scripts and meta): *[GitHub](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19)*
* CM automation "script": *[Docs](https://github.com/octoml/ck/blob/master/docs/list_of_automations.md#script)*

___
### Meta description
[_cm.json](_cm.json)

___
### Tags
get,dataset,medical-imaging,kits,original,kits19

___
### Variations
#### All variations
* calibration
  - *ENV CM_DATASET_CALIBRATION*: `yes`
* default
  - *ENV CM_GIT_PATCH*: `no`
* full-history
  - *ENV CM_GIT_DEPTH*: ``
* no-recurse-submodules
  - *ENV CM_GIT_RECURSE_SUBMODULES*: ``
* patch
  - *ENV CM_GIT_PATCH*: `yes`
* short-history
  - *ENV CM_GIT_DEPTH*: `--depth 5`
* validation
  - *ENV CM_DATASET_VALIDATION*: `yes`
___
### Versions
Default version: *master*

* custom
* master
___
### Default environment

* CM_GIT_CHECKOUT: **master**
* CM_GIT_DEPTH: **--depth 4**
* CM_GIT_PATCH: **no**
* CM_GIT_RECURSE_SUBMODULES: ****
* CM_GIT_URL: **https://github.com/neheller/kits19**
___
### CM script workflow

  1. ***Read "deps" on other CM scripts from [meta](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/_cm.json)***
     * detect,os
       - CM script: [detect-os](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/detect-os)
  1. ***Run "preprocess" function from [customize.py](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/customize.py)***
  1. Read "prehook_deps" on other CM scripts from [meta](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/_cm.json)
  1. ***Run native script if exists***
     * [run.sh](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/run.sh)
  1. Read "posthook_deps" on other CM scripts from [meta](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/_cm.json)
  1. ***Run "postrocess" function from [customize.py](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/customize.py)***
  1. Read "post_deps" on other CM scripts from [meta](https://github.com/mlcommons/ck/tree/master/cm-mlops/script/get-dataset-kits19/_cm.json)
___
### New environment export

* **CM_DATASET_***
___
### New environment detected from customize

* **CM_DATASET_PATH**
* **CM_GIT_CHECKOUT**
* **CM_GIT_DEPTH**
* **CM_GIT_RECURSE_SUBMODULES**
___
### Usage

#### CM installation
[Guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md)

#### CM script automation help
```cm run script --help```

#### CM CLI
`cm run script --tags="get,dataset,medical-imaging,kits,original,kits19"`

*or*

`cm run script "get dataset medical-imaging kits original kits19"`

*or*

`cm run script 79992bb221024ac5`

#### CM Python API

```python
import cmind

r = cmind.access({'action':'run'
                  'automation':'script',
                  'tags':'get,dataset,medical-imaging,kits,original,kits19'
                  'out':'con',
                  ...
                  (other input keys for this script)
                  ...
                 })

if r['return']>0:
    print (r['error'])
```

#### CM modular Docker container
*TBD*
___
### Maintainers

* [Open MLCommons taskforce on education and reproducibility](https://github.com/mlcommons/ck/blob/master/docs/mlperf-education-workgroup.md)