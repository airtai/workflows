# Docusaurus GHP deploy action file for [fastkafka](https://github.com/airtai/fastkafka)

## Getting started

Update your deploy workfow file `.github/workflows/deploy.yml` to use `airtai/workflows/fastkafka-docusaurus-ghp@main` and push it to your remote default branch for generating documentation using docusaurus.

Here is an example worfklow

```yaml
name: Deploy docusaurus generated documentation to GitHub Pages

on:
  push:
    branches: [ "main", "master" ]
  workflow_dispatch:
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: airtai/workflows/fastkafka-docusaurus-ghp@main
```