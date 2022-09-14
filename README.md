# Multiple Language Github Action Workflow
I created an github action workflow for 4 language programing: Rust, Go, Python, Nodejs

## Tutorial
- Create github action file.
- Use workflow: trivonhan/multi-lang-github-action/.github/workflows/main.yml@master
* Example:
```bash
name: Nodejs CI

on:
  push:
    tags:
      - v*
    branches:
      - master
      - main
      - feat/**
  pull_request:
  
jobs:
  nodejs_ci:
    uses: trivonhan/multi-lang-github-action/.github/workflows/main.yml@master
    with:
      language: 'nodejs'
      package_manager: 'pnpm'
 ```
 - Must specify `languge`, `package_manager` is optional.
 - `language` is now suporting `Rust`, `Go`, `Nodejs`, `Python`
 - `package_manager` is now supporting `npm`, `yarn`, `pnpm`
 
