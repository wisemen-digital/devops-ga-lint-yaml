# Lint YAML

Lints all YAML files in the repository (or only the given paths). Will use a default config if none exists in the repo.

## Input

```yaml
inputs:
  paths:
    description: Paths to lint
    required: false
```

## Usage

```yaml
name: Pull Request
on:
  push:
    branches: [ main ]
  workflow_dispatch:

jobs:
  lint:
    steps:
      - uses: wisemen-digital/devops-ga-lint-yaml@main
  
  lint-only-github:
    steps:
      - uses: wisemen-digital/devops-ga-lint-yaml@main
        with:
          paths: >
            .github
```
