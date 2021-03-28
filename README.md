# Web Extension starter

![Icon](./dist/icon128.png)

A simple starter for creating web extensions for Chrome and Firefox

The starter uses

- `styled-components` for styling
- `jest` and `testing-library-react` for tests
- `webextension-polyfill-ts` to polyfill the differences of Chrome and Firefox. Write once run everywhere™️

## Requirements

To be able to run the extension you need

- Node.js version 14.x or higher
- Yarn version 1.x

## Setting up

1. `yarn install` installs the required dependencies.
2. `yarn watch` starts the dev webpack process, that will watch the TypeScript source code and compile it to `./dist/js` on each new file save.
3. `yarn extension` starts development of the extension locally on your default browser. This uses [web-ext](https://github.com/mozilla/web-ext) and installs the extension in development mode on the browser. `web-ext` watches the output folder (./dist/js) of the webpack process and automatically reloads everytime there is an update to the compiled output.
4. To start one of the browsers individually run
   1. `yarn chrome` for Chrome
   2. `yarn firefox` for Firefox

## Browser

The browser instances are started with new profile and settings that are stored in `.chrome` and `.firefox` folders. This enables to make changes to the browser settings that are persisted in those folders.

## Production build

To build a production version of the source code, run `yarn build`. This will output the code into `./dist/js`

## Tests

To run unit tests locally run `yarn test`

## Linting

To run the linter run `yarn lint`
