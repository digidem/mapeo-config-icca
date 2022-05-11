## Get started

You will need [Node v12 or later](https://nodejs.org/en/) installed, then clone this repo and change into the folder you have cloned into:

```sh
git clone https://github.com/digidem/mapeo-config-icca.git
cd mapeo-config-icca
```

Then install dependencies with `npm` (npm is installed with Node)

```sh
npm install
```

## Running config locally and adding changes

1. Make changes to the code write all commits as conventional commits (https://www.conventionalcommits.org/en/v1.0.0/)

2. Set up locally mapeo desktop or/and mobile (https://github.com/digidem/mapeo-desktop/)

3. Export and build the config

```sh
npm run extract-messages
npm run build
```

4. Import the config to mapeo desktop or/and mobile (you can do it in UI from the menu)

This will generate a file in build/config-icca-vX.X.X.mapeosettings. You can import this into Mapeo Desktop following these instructions: https://docs.mapeo.app/complete-reference-guide/mapeo-desktop-installation-setup/importing-configurations


## Publishing config on npm
1. Merge changes to master, checkout master ?

```sh
npm install
```

2. Pick a version type (otherwise you need to bump the version number by using npm version patch|minor|major - Read up on “semver” if those terms don’t mean much to you.)

```sh
npx standard-version
```

```sh
git push --follow-tags origin master && npm publish
```
