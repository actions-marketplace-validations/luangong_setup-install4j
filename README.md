# setup-install4j

[![CI](https://github.com/luangong/setup-install4j/actions/workflows/ci.yml/badge.svg)](https://github.com/luangong/setup-install4j/actions/workflows/ci.yml)

This action provides the following functionality for GitHub Actions runners:

- Downloading and setting up a requested version of [install4j](https://www.ej-technologies.com/products/install4j/overview.html)
- Caching downloaded JRE bundles

After setting up install4j, its bin directory will be added to PATH, so you can run commands like `createbundle` or `install4jc` directly.

## Usage

```yml
steps:
  - uses: luangong/setup-install4j@v1
    with:
      version: 10.0.4
      license: ${{ secrets.INSTALL4J_LICENSE }}
```

Currently, install4j v9 and newer are supported.

<!--
### Caching JREs

The action has a built-in functionality for caching and restoring JREs for bundling.  It uses [actions/cache](https://github.com/actions/cache) under the hood for caching JRE bundles but requires less configuration settings.  See the [JRE Bundles](https://www.ej-technologies.com/resources/install4j/help/doc/concepts/jreBundles.html) section of the official documentation for more details.
-->

## TODOs

- [ ] Handle semantic version specifications
- [ ] Implement caching of downloaded JREs
- [ ] Take advantage of tool cache
- [ ] Cleaning up
