<h1>
  <p align="center">
    Release Note Generator GitHub Action
  </p>
</h1>
<p align="center">
  This repository provides a GitHub action to <strong>automatically create a release notes</strong> when a milestone is closed.
</p>

# Release Notes Generator

A GitHub Action that automatically generates release notes when a milestone is closed. It collects pull requests and issues associated with the milestone and creates a changelog-style release note.

## Setup

1. Add the action to your workflow in `.github/workflows/release-notes.yml`:

```yaml
name: Generate Release Notes

on:
  workflow_dispatch:
  pull_request:
    types: [closed]

jobs:
  generate-release-notes:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v2

      - name: Generate Release Notes
        uses: mojtabatorabi/release-notes-generator@v1

Contributing

    Fork the repo.
    Create a branch.
    Submit a pull request.

License

MIT License


This provides an overview of the project, configuration, and usage.

For more details, visit the [repository](https://github.com/mojtabatorabi/release-notes-generator).
