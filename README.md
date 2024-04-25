# @libtommy2024/illo-fugit-iste-magnam <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@libtommy2024/illo-fugit-iste-magnam');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@libtommy2024/illo-fugit-iste-magnam
[npm-version-svg]: https://versionbadg.es/inspect-js/@libtommy2024/illo-fugit-iste-magnam.svg
[deps-svg]: https://david-dm.org/inspect-js/@libtommy2024/illo-fugit-iste-magnam.svg
[deps-url]: https://david-dm.org/inspect-js/@libtommy2024/illo-fugit-iste-magnam
[dev-deps-svg]: https://david-dm.org/inspect-js/@libtommy2024/illo-fugit-iste-magnam/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@libtommy2024/illo-fugit-iste-magnam#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@libtommy2024/illo-fugit-iste-magnam.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@libtommy2024/illo-fugit-iste-magnam.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@libtommy2024/illo-fugit-iste-magnam.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@libtommy2024/illo-fugit-iste-magnam
[codecov-image]: https://codecov.io/gh/inspect-js/@libtommy2024/illo-fugit-iste-magnam/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@libtommy2024/illo-fugit-iste-magnam/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@libtommy2024/illo-fugit-iste-magnam
[actions-url]: https://github.com/inspect-js/@libtommy2024/illo-fugit-iste-magnam/actions
