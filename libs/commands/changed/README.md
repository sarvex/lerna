# `lerna changed`

> List local packages that have changed since the last tagged release

Install [lerna](https://www.npmjs.com/package/lerna) for access to the `lerna` CLI.

## Usage

The output of `lerna changed` is a list of packages that would be the subjects of the next `lerna version` or `lerna publish` execution.

```sh
$ lerna changed
package-1
package-2
```

**Note:** `lerna.json` configuration for `lerna publish` _and_ `lerna version` also affects
`lerna changed`, e.g. `command.publish.ignoreChanges`.

## Options

`lerna changed` supports all of the flags supported by [`lerna ls`](https://github.com/lerna/lerna/tree/main/libs/commands/list#options):

- [`--json`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--json)
- [`--ndjson`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--ndjson)
- [`-a`, `--all`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--all)
- [`-l`, `--long`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--long)
- [`-p`, `--parseable`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--parseable)
- [`--toposort`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--toposort)
- [`--graph`](https://github.com/lerna/lerna/tree/main/libs/commands/list#--graph)

Unlike `lerna ls`, however, `lerna changed` **does not** support [filter options](https://www.npmjs.com/package/@lerna/filter-options), as filtering is not supported by `lerna version` or `lerna publish`.

`lerna changed` supports the following options of [`lerna version`](https://github.com/lerna/lerna/tree/main/libs/commands/version#options) (the others are irrelevant):

- [`--conventional-graduate`](https://github.com/lerna/lerna/tree/main/libs/commands/version#--conventional-graduate).
- [`--force-publish`](https://github.com/lerna/lerna/tree/main/libs/commands/version#--force-publish).
- [`--ignore-changes`](https://github.com/lerna/lerna/tree/main/libs/commands/version#--ignore-changes).
- [`--include-merged-tags`](https://github.com/lerna/lerna/tree/main/libs/commands/version#--include-merged-tags).
