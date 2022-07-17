# github-labels-presets

GitHub Labels presets for [github-labels-sync-action](https://github.com/r7kamura/github-label-sync-action).

## Usage

```yaml
# .github/workflows/github-label-sync.yml
name: github-label-sync

on:
  push:
    branches:
      - main
    paths:
      - .github/labels.yml
      - .github/workflows/github-label-sync.yml
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: r7kamura/github-label-sync-action@v0
        with:
          source_path: labels-keepachangelog.yml
          source_repository: r7kamura/github-labels-preset
```

## Presets

### labels-keepachangelog.yml

Labels based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
