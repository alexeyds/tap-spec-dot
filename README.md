Forked [tap-spec](https://github.com/scottcorgan/tap-spec) TAP reporter, but with dots for passing tests

![](https://i.imgur.com/Gl0bbvO.png)

## Install

```
npm install tap-spec-dot --save-dev
```

## Usage

### Streaming

```js
var test = require('tape');
var tapSpec = require('tap-spec-dot');

test.createStream()
  .pipe(tapSpec())
  .pipe(process.stdout);
```

### CLI

**package.json**

```json
{
  "name": "module-name",
  "scripts": {
    "test": "node ./test/tap-test.js | tap-spec-dot"
  }
}
```

Then run with `npm test`

**Terminal**

```
tape test/index.js | node_modules/.bin/tap-spec-dot
```

**Testling**

```
npm install testling -g
testling test/index.js | node_modules/.bin/tap-spec-dot
```
