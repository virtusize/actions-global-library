# Github actions global library

## Versions

You can specify the version you want to use by the github tag in this repo.
`virtusize/actions-global-library/.github/workflows/changelog.yml@v2.0.0` If `v2.0.0` exists as tag.

#### Examples

- **Golang:** [compile + release notes](https://github.com/virtusize/terraform-provider-clickhouse/blob/main/.github/workflows/release.yml)


## Usage

```yml
...
jobs:
  ...
  release-notes:
    name: 'Create release notes from CHANGELOG.md'
    uses: virtusize/actions-global-library/.github/workflows/release-notes.yml
  ...
  changelog:
    name: 'Changelog release'
    uses: virtusize/actions-global-library/.github/workflows/changelog.yml
    needs: [release-notes, example-job]
    with:
      update-changelog: false
...
```
