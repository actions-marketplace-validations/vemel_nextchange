# Keep a Changelog action

Parse and update CHANGELOG.md

- [Keep a Changelog action](#keep-a-changelog-action)
  - [Usage](#usage)
    - [Pre-requisites](#pre-requisites)
    - [Inputs](#inputs)
    - [Outputs](#outputs)
  - [Examples](#examples)
  - [Contributing](#contributing)
  - [License](#license)

## Usage
### Pre-requisites
Create a workflow `.yml` file in your repositories `.github/workflows` directory. Check [Examples](#examples) below. For more information, reference the GitHub Help Documentation for [Creating a workflow file](https://help.github.com/en/articles/configuring-a-workflow#creating-a-workflow-file).

### Inputs
| Name | Default | Description |
| - | - | - |
| `path` | `"./CHANGELOG.md"` | Path to `CHANGELOG.md` file |
| `get` | `"Unreleased"` | Get target release by its version |
| `release` | `""` | If provided, create a new release with given version from target release |
| `set` | `""` | Fully replace target release notes |
| `append` | `""` | Append new lines to target release notes |
| `suffix` | `""` | Add suffix to each section of `set`/`append` notes, good for pasting a link to PR |
| `save` | `"true"` | Whether to save changes back to `CHANGELOG.md` path |
| `sanitize` | `"false"` | Keep only `Keep a Changelog` sections in release notes |
| `encoding` | `"utf-8"` | Encoding for `CHANGELOG.md` |

### Outputs
| Name | Example | Description |
| - | - | - |
| `result` | `"### Added ..."` | Target Release notes |
| `label` | `"minor"` | Release label based on release notes: `major`, `minor`, or `patch` |
| `titles` | `"added,removed,fixed"` | Comma-separated `Keep a Changelog` titles from release notes |


## Examples
- [Python: Bump version on demand](examples/python-on-demand.yml)
- [Python: Bump version on release published](examples/python-on-release-published.yml)
- [Node.js: Bump version on demand](examples/nodejs-on-demand.yml)
- [Node.js: Bump version on release published](examples/pnodejs-on-release-published.yml)


## Contributing
I would love for you to contribute to `actions/keepachangelog`, pull requests are welcome! Please see the [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## License
The scripts and documentation in this project are released under the [MIT License](LICENSE)