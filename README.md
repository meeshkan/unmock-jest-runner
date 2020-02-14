# unmock-jest-runner

[![CircleCI Status](https://circleci.com/gh/Meeshkan/unmock-jest-runner.svg?style=svg)](https://circleci.com/gh/Meeshkan/unmock-jest-runner)

With the [Unmock `runner`](https://github.com/Meeshkan/unmock-js/tree/dev/packages/unmock-runner), you can run any test multiple times with different potential outcomes from the API.

This package holds the core functions for the Jest configuration of the `runner`.

### Default

By default, the `runner` is set to run your test 20 times.

### Usage

The `unmock-jest-runner` can be installed via NPM or Yarn:

```
npm install -D unmock-jest-runner
yarn add unmock-jest-runner
```

Once installed, the `runner` can be imported as a default and used as a wrapper for your tests:

```js
const runner = require("unmock-jest-runner").default;

test("my API always works as expected", runner(async () => {
  const res = await myApiFunction();
  // some expectations
}));
```

### Beyond Jest

As of now, Jest is the only package available for the Unmock `runner`. 

However, we're currently building out support for [Mocha](https://github.com/Meeshkan/unmock-js/issues/299) and [QUnit](https://github.com/Meeshkan/unmock-js/issues/300). You can follow the progress of those implementations in the corresponding issues.