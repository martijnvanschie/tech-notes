# Npm Package Manager

## Updating packages

### Updating to the latest

### Update to the newest

`npm update` will not update to the `@latest` version but to the last version that matches the latest based on the [version rule](https://flaviocopes.com/npm-semantic-versioning/).

To update to the `@latest`version you first need to update the versions in the `package.json` file. There is a npm package that does this automatically for you called `npm-check-updates`.

First you need to install the package globally.

```bash
npm install -g npm-check-updates
```

Then from you project folder run the following command to check for the possible updates

```bash
ncu
```

This will output all packages that have updates available.

Then you can run the following command. This will update you `package.json`with the latest version.

```bash
ncu -u
```

Now we need to update all the packages with the latest changed version

```bash
npm install
```

**Resources**

https://flaviocopes.com/update-npm-dependencies/

https://www.npmjs.com/package/npm-check-updates

