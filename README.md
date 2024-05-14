# package-version-upgrade-check

This action check if the package version in the package.json file of source branch is greater than the package version in the package.json file of target branch.

## About me
I am a full-stack software engineer. I have experience in building and maintaining various projects. I am always looking for ways to automate and improve the development process.

## Contact Information
If you have any questions, suggestions or need help, please follow and contact me at:
- [LinkedIn](https://www.linkedin.com/in/bakhrom-akbarov/)

## Example usage:
#### 1. Applies to pull_request to main branch only.

```
name: If the package version is greater than the main branch version

on:
  pull_request:
    branches:
      - main

jobs:
  #  This job checks if the package version is greater than the main branch version and checks if the package can be built.
  version_check:
    if: ${{ github.event_name == 'pull_request' }}
    runs-on: ubuntu-latest
    steps:
      - uses: bakhrom-akbarov/package-version-upgrade-check@v1.0.3
```

#### 2. Applies to pull_request to any branch.

```
name: If the package version is greater than the target branch version

on:
  pull_request
    branches:
      - '**'

jobs:
  #  This job checks if the package version is greater than the main branch version and checks if the package can be built.
  version_check:
    if: ${{ github.event_name == 'pull_request' }}
    runs-on: ubuntu-latest
    steps:
      - uses: bakhrom-akbarov/package-version-upgrade-check@v1.0.3
```
