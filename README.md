<p align="center">
  <h3 align="center">Buildtool Deploy Action</h3>
  <p align="center"><a href="https://github.com/features/actions">GitHub Action</a> for <a href="https://buildtools.io/commands/#deploy">Buildtool Deploy</a></p>
  <p align="center">
    <a href="https://github.com/buildtool/deploy-action/releases/latest"><img alt="GitHub release" src="https://img.shields.io/github/release/buildtool/deploy-action.svg?logo=github"></a>
    <a href="https://github.com/marketplace/actions/github-action-for-deploy"><img alt="GitHub marketplace" src="https://img.shields.io/badge/marketplace-deploy--action-blue?logo=github"></a>
  </p>
</p>

---

> **:warning: Note:** To use this action, you must have access to the [GitHub Actions](https://github.com/features/actions) feature. GitHub Actions are currently only available in public beta. You can [apply for the GitHub Actions beta here](https://github.com/features/actions/signup/).

## Usage

Below is a simple snippet to use this action.

```yaml
name: buildtool

on:
  pull_request:
  push:

jobs:
  goreleaser:
    runs-on: ubuntu-latest
    steps:
      -
        name: Checkout
        uses: actions/checkout@v1
      -
        name: Run build-tools deploy command
        uses: buildtool/deploy-action@v1
        with:
          target: production
```

## Customizing

### Inputs

Following inputs can must be provided as `step.with` keys

| Name         | Type    |  Description                                   |
|--------------|---------|------------------------------------------------|
| `target`     | String  | Which target [environment] to deploy to        |


## License

MIT. See `LICENSE` for more details.

[environment]: https://buildtools.io/environments/