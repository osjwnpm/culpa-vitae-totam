# @osjwnpm/culpa-vitae-totam <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][5]][6]
[![dev dependency status][7]][8]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Typed Array? This module works cross-realm/iframe, does not depend on `instanceof` or mutable properties, and despite ES6 Symbol.toStringTag.

## Example

```js
var isTypedArray = require('@osjwnpm/culpa-vitae-totam');
var assert = require('assert');

assert.equal(false, isTypedArray(undefined));
assert.equal(false, isTypedArray(null));
assert.equal(false, isTypedArray(false));
assert.equal(false, isTypedArray(true));
assert.equal(false, isTypedArray([]));
assert.equal(false, isTypedArray({}));
assert.equal(false, isTypedArray(/a/g));
assert.equal(false, isTypedArray(new RegExp('a', 'g')));
assert.equal(false, isTypedArray(new Date()));
assert.equal(false, isTypedArray(42));
assert.equal(false, isTypedArray(NaN));
assert.equal(false, isTypedArray(Infinity));
assert.equal(false, isTypedArray(new Number(42)));
assert.equal(false, isTypedArray('foo'));
assert.equal(false, isTypedArray(Object('foo')));
assert.equal(false, isTypedArray(function () {}));
assert.equal(false, isTypedArray(function* () {}));
assert.equal(false, isTypedArray(x => x * x));
assert.equal(false, isTypedArray([]));

assert.ok(isTypedArray(new Int8Array()));
assert.ok(isTypedArray(new Uint8Array()));
assert.ok(isTypedArray(new Uint8ClampedArray()));
assert.ok(isTypedArray(new Int16Array()));
assert.ok(isTypedArray(new Uint16Array()));
assert.ok(isTypedArray(new Int32Array()));
assert.ok(isTypedArray(new Uint32Array()));
assert.ok(isTypedArray(new Float32Array()));
assert.ok(isTypedArray(new Float64Array()));
assert.ok(isTypedArray(new BigInt64Array()));
assert.ok(isTypedArray(new BigUint64Array()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@osjwnpm/culpa-vitae-totam
[npm-version-svg]: https://versionbadg.es/inspect-js/@osjwnpm/culpa-vitae-totam.svg
[deps-svg]: https://david-dm.org/inspect-js/@osjwnpm/culpa-vitae-totam.svg
[deps-url]: https://david-dm.org/inspect-js/@osjwnpm/culpa-vitae-totam
[dev-deps-svg]: https://david-dm.org/inspect-js/@osjwnpm/culpa-vitae-totam/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@osjwnpm/culpa-vitae-totam#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@osjwnpm/culpa-vitae-totam.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@osjwnpm/culpa-vitae-totam.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@osjwnpm/culpa-vitae-totam.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@osjwnpm/culpa-vitae-totam
[codecov-image]: https://codecov.io/gh/inspect-js/@osjwnpm/culpa-vitae-totam/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@osjwnpm/culpa-vitae-totam/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@osjwnpm/culpa-vitae-totam
[actions-url]: https://github.com/osjwnpm/culpa-vitae-totam/actions
