# GitHub Pages deploy action file for [fastkafka](https://github.com/airtai/fastkafka)

## Getting started

Add your workfow file `.github/workflows/fastkafka_docs_deploy.yml` and push it to your remote default branch.

Here is an example worfklow

```yaml
name: Deploy fastkafka generated documentation to GitHub Pages

on:
  push:
    branches: [ "main", "master" ]
  workflow_dispatch:
jobs:
  deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: airtai/workflows/fastkafka-ghp@main
        with:
          app: "test_fastkafka.application:kafka_app"
```

## Options

### Set app location

Input in the form of `path:app`, where `path` is the path to a python file and `app` is an object of type `FastKafka`

```yaml
- name: Deploy
  uses: airtai/workflows/fastkafka-ghp@main
  with:
    app: "test_fastkafka.application:kafka_app"
```

In the above example, FastKafka app is named as "kafka_app" and it is available in "application" which is a submodule of "test_fastkafka" module
