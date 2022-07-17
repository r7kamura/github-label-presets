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
          path: github-default.yml
          repository: r7kamura/github-labels-keepachangelog
```
