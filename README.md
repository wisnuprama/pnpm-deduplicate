# pnpm-deduplicate

Remove duplicate dependencies from `pnpm-lock.yaml`.

This project is simple and not have many features. I see it as a temporary solution until we have built-in `pnpm deduple` command. Pull requests are welcome!

## Install

```
pnpm install -g pnpm-deduplicate
```

## Usage

### Remove duplicates

Go to your project's root directory and run the following command to remove duplicate dependencies:

```
pnpm-deduplicate
```

### List duplicates

If you only want to list duplicates instead of update `pnpm-lock.yaml`, run:

```
pnpm-deduplicate --list
```

You will get a list of duplicates like this:

```
Package "@babel/core" wants ^7.17.10 and could get 7.18.2, but got 7.18.0
Package "@babel/core" wants ^7.15.5 and could get 7.18.2, but got 7.18.0
Package "@babel/core" wants ^7.7.5 and could get 7.18.2, but got 7.18.0
Package "@babel/generator" wants ^7.7.2 and could get 7.18.2, but got 7.18.0
Package "@babel/generator" wants ^7.18.0 and could get 7.18.2, but got 7.18.0
```

## Solutions for other package managers

For Yarn v1, you can use [`yarn-deduplicate`](https://github.com/atlassian/yarn-deduplicate/).

For Yarn v2 or greater version, you can use the built-in [`yarn dedupe`](https://yarnpkg.com/cli/dedupe) command.

For NPM, you can use the built-in [`npm dedupe`](https://docs.npmjs.com/cli/v8/commands/npm-dedupe) command.

## License

MIT
