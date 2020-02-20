# About
This repository contains utilities for testing Besu database migration scenarios.

# Overview

## Setup
These scripts assume some dependencies are installed locally:

* Docker
* JQ
  * On mac, jq can be installed via homebrew
  * See: [jq docs](https://stedolan.github.io/jq/download/)

## Basic workflow
Edit files in the `input` folder to specify desired chain data.

Scripts for running test cases are in `scripts`.
From the root directory of this repo, execute the desired test suite file:
```
sh scripts/run-migration-test-suite
```

Sample output:
```
[Before_Versioning_Was_Enabled] expected blockNumber: 0xA
[Before_Versioning_Was_Enabled] actual blockNumber: 0xa
[Before_Versioning_Was_Enabled] expected balance: 0x2b5e3af16b1880000
[Before_Versioning_Was_Enabled] actual balance: 0x2b5e3af16b1880000
[After_Versioning_Was_Enabled] expected blockNumber: 0xA
[After_Versioning_Was_Enabled] actual blockNumber: 0x9
[After_Versioning_Was_Enabled] expected balance: 0x2b5e3af16b1880000
[After_Versioning_Was_Enabled] actual balance: 0x270801d946c940000
```
