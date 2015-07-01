[![NPM Version](http://img.shields.io/npm/v/debouncy.svg?style=flat)](https://npmjs.org/package/debouncy)
[![Build Status](http://img.shields.io/travis/royriojas/debouncy.svg?style=flat)](https://travis-ci.org/royriojas/debouncy)

# debouncy
Yet another debounce implementation with 0 dependencies

## Install

```bash
npm i --save debouncy
```

## Usage

```javascript
var debouncy = require('debouncy');

var debouncedFn = debouncy(function () { console.log('I am called') }, 200);
debounceFn();
// after 200ms
// output: I am called
var ctx = {
  name: 'some obj';
}
var debouncedFn = debouncy(function () { console.log('I am called from', this.name) }, 200, ctx);
debounceFn();
// after 200ms
// output: I am called from some obj

var debouncedFn = debouncy(function () { console.log('I am called') }, 200, null, true /*immediate*/);
debounceFn();
// immediately
// output: I am called
// other calls will have to wait 200ms before the last execution
```

## Changelog
[changelog](./changelog.md)

## License
[MIT](./LICENSE)
