# go-repo-template

[![Code Analysis](https://github.com/sv-tools/go-repo-template/actions/workflows/checks.yaml/badge.svg)](https://github.com/sv-tools/go-repo-template/actions/workflows/checks.yaml)
[![Go Reference](https://pkg.go.dev/badge/github.com/sv-tools/go-repo-template.svg)](https://pkg.go.dev/github.com/sv-tools/go-repo-template)
[![codecov](https://codecov.io/gh/sv-tools/go-repo-template/branch/main/graph/badge.svg?token=0XVOTDR1CW)](https://codecov.io/gh/sv-tools/go-repo-template)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/sv-tools/go-repo-template?style=flat)](https://github.com/sv-tools/go-repo-template/releases)

The template for new go repository.

## Features

1. MIT License by default
2. GitHub Action workflows:
    1. testing all pull requests by running same tools for stable and previous Go version and checking code coverage
       using `codecov` action
    2. checking code quality by running `golangci-lint` action
    3. making a new release by running `goreleaser` action when a new tag is pushed

## Usage

1. Create a repository using this repo as template
2. Replace in all files `go-repo-template` to the project's name
3. Replace `sv-tools` to the project's owner
4. In case of library:
    1. Remove `.github/Dockerfile`, `.github/goreleaser-cli.yml` files
    2. Remove `release-cli` section in the `.github/workflows/release.yaml` file
5. Modify `README.md` by removing this text
6. Feel free to modify any other files

## Recommendations

Set up branch protection rules for the main branch and configure to run CodeQL analysis.

## License

MIT licensed. See the bundled [LICENSE](LICENSE) file for more details.
