# vaporyjs-units

[![NPM Package](https://img.shields.io/npm/v/vaporyjs-units.svg?style=flat-square)](https://www.npmjs.org/package/vaporyjs-units)
[![Build Status](https://img.shields.io/travis/vaporyjs/vaporyjs-units.svg?branch=master&style=flat-square)](https://travis-ci.org/vaporyjs/vaporyjs-units)
[![Coverage Status](https://img.shields.io/coveralls/vaporyjs/vaporyjs-units.svg?style=flat-square)](https://coveralls.io/r/vaporyjs/vaporyjs-units)
[![Gitter](https://img.shields.io/gitter/room/vapory/vaporyjs-lib.svg?style=flat-square)](https://gitter.im/vapory/vaporyjs-lib) or #vaporyjs on freenode

Unit conversion utility.

There are two methods:

- `convert(value, unitFrom, unitTo)` - convert a value between two units
- `lazyConvert(value, unitTo)` - include unit type in the input and the output

The `value` and the output in all cases is a string.

## Examples

```js
Units.convert('1', 'vap', 'wei') // '1000000000000000000'
Units.convert('1', 'wei', 'vap') // '0.000000000000000001'
Units.convert('1', 'finney', 'vap') // '0.001'

Units.lazyConvert('1 vap', 'wei') // '1000000000000000000 wei'
Units.lazyConvert('1 wei', 'vap') // '0.000000000000000001 vap'
Units.lazyConvert('1 finney', 'vap') // '0.001 vap'
```

## Units

Units are defined in `units.json`. It is compatible with [web3.js](https://github.com/vaporyco/web3.js) and additionally includes `VAP`.
