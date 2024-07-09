# Cache and Install apt (.deb) Packages

This GitHub Action caches and installs .deb packages.

## Inputs

### `package-list`

**Required** A space-separated list of apt (.deb) packages to install.

## Example Usage

```yaml
name: Cache and Install apt (.deb) Packages

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  install_packages:
    runs-on: ubuntu-latest

    steps:
    - name: Cache and Install apt (.deb) Packages
      uses: eth-pkg/apt-deb-cache@v0.2.2
      with:
        packages: 'curl git'

```
