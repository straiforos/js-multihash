# js-multihash <!-- omit in toc -->

[![](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat-square)](http://ipn.io)
[![](https://img.shields.io/badge/project-multiformats-blue.svg?style=flat-square)](https://github.com/multiformats/multiformats)
[![](https://img.shields.io/badge/freenode-%23ipfs-blue.svg?style=flat-square)](https://webchat.freenode.net/?channels=%23ipfs)
[![Coverage Status](https://coveralls.io/repos/github/multiformats/js-multihash/badge.svg?branch=master)](https://coveralls.io/github/multiformats/js-multihash?branch=master)
[![Travis CI](https://img.shields.io/travis/multiformats/js-multihash.svg?style=flat-square&branch=master)](https://travis-ci.org/multiformats/js-multihash)
[![Dependency Status](https://david-dm.org/multiformats/js-multihash.svg?style=flat-square)](https://david-dm.org/multiformats/js-multihash)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/feross/standard)
[![](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> multihash implementation in node.js

This is the [multihash](//github.com/multiformats/multihash) implementation in Node.
It is extended by [js-multihashing](https://github.com/multiformats/js-multihashing)
and [js-multihashing-async](https://github.com/multiformats/js-multihashing-async),
so give those a look as well.

## Lead Maintainer <!-- omit in toc -->

[Hugo Dias](http://github.com/hugomrdias/)

## Table of Contents <!-- omit in toc -->

- [Install](#install)
  - [Using npm](#using-npm)
  - [Using a `<script>` tag](#using-a-script-tag)
- [Usage](#usage)
- [API](#api)
- [Update Constants](#update-constants)
- [Contribute](#contribute)
- [License](#license)

## Install

### Using npm

```bash
> npm install multihashes # node the name of the module is multihashes
```

Once the install is complete, you can require it as a normal dependency

```js
const multihashes = require('multihashes')
```

You can require it and use with your favourite bundler to bundle this package in a browser compatible code.

### Using a `<script>` tag

Loading this module through a script tag will make the ```Multihashes``` obj available in the global namespace.

```html
<script src="https://unpkg.com/multihashes/dist/index.min.js"></script>
```

## Usage

```js
> var multihash = require('multihashes')
> var bytes = Uint8Array.from([0, 1, 2, 3...])

> var encoded = multihash.encode(bytes, 'sha1')
> console.log(encoded)
<Uint8Array 11 14 0b ee c7 b5 ea 3f 0f db c9 5d 0d d4 7f 3c 5b c2 75 da 8a 33>

> multihash.decode(encoded)
{ code: 17,
  name: 'sha1',
  length: 20,
  digest: <Uint8Array 0b ee c7 b5 ea 3f 0f db c9 5d 0d d4 7f 3c 5b c2 75 da 8a 33> }
```

## API

https://multiformats.github.io/js-multihash/

## Update Constants

To update the constants table run the command below. This will fetch the main codec list from https://raw.githubusercontent.com/multiformats/multicodec/master/table.csv and filter only the multihash codecs and update the `constants.js` file in this repo.

```sh
npm run update-constants
```


## Contribute

Contributions welcome. Please check out [the issues](https://github.com/multiformats/js-multihash/issues).

Check out our [contributing document](https://github.com/multiformats/multiformats/blob/master/contributing.md) for more information on how we work, and about contributing in general. Please be aware that all interactions related to multiformats are subject to the IPFS [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md).

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

[MIT](LICENSE) © Protocol Labs Inc.
