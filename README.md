# R package build and test action

This action is designed to automatically run build and check for R packages on their code with every commit.

## Example Usage
To get this action running in your project, add the following config to .github/workflows/frcbuild.yml:
```yml
name: R Build and Checks
on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-18.04
    steps:
    - uses: actions/checkout@master
    - name: R Build and Checks
      uses: Swechhya/R-actions@master
      with:
        action: 'all'
```

The action property can be any one of:
- `build` Only builds the package
- `all` Runs build and checks the built package

