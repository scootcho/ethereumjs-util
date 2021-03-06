# SYNOPSIS

[![NPM Package](https://img.shields.io/npm/v/ethereumjs-util.svg)](https://www.npmjs.org/package/ethereumjs-util)
[![Actions Status](https://github.com/ethereumjs/ethereumjs-util/workflows/Build/badge.svg)](https://github.com/ethereumjs/ethereumjs-util/actions)
[![Coverage Status](https://img.shields.io/coveralls/ethereumjs/ethereumjs-util.svg)](https://coveralls.io/r/ethereumjs/ethereumjs-util)
[![Gitter](https://img.shields.io/gitter/room/ethereum/ethereumjs-lib.svg)](https://gitter.im/ethereum/ethereumjs-lib)

A collection of utility functions for Ethereum. It can be used in Node.js and in the browser with [browserify](http://browserify.org/).

# INSTALL

`npm install ethereumjs-util`

# USAGE

```js
import assert from 'assert'
import { isValidChecksumAddress, unpad, BN } from 'ethereumjs-util'

const address = '0x2F015C60E0be116B1f0CD534704Db9c92118FB6A'
assert.ok(isValidChecksumAddress(address))

assert.equal(unpad('0000000006600'), '6600')

assert.equal(new BN('dead', 16).add(new BN('101010', 2)), 57047)
```

# API

## Documentation

### Modules

- [account](docs/modules/_account_.md)
  - Private/public key and address-related functionality (creation, validation, conversion)
- [bytes](docs/modules/_bytes_.md)
  - Byte-related helper and conversion functions
- [constants](docs/modules/_constants_.md)
  - Exposed constants
    - e.g. KECCAK256_NULL_S for string representation of Keccak-256 hash of null
- [hash](docs/modules/_hash_.md)
  - Hash functions
- [object](docs/modules/_object_.md)
  - Helper function for creating a binary object (`DEPRECATED`)
- [signature](docs/modules/_signature_.md)
  - Signing, signature validation, conversion, recovery
- [externals](docs/modules/_externals_.md)
  - Helper methods from `ethjs-util`
  - Re-exports of `BN`, `rlp`

### ethjs-util methods

The following methods are available provided by [ethjs-util](https://github.com/ethjs/ethjs-util):

- arrayContainsArray
- toBuffer
- getBinarySize
- stripHexPrefix
- isHexPrefixed
- isHexString
- padToEven
- intToHex
- fromAscii
- fromUtf8
- toUtf8
- toAscii
- getKeys

### Re-Exports

Additionally `ethereumjs-util` re-exports a few commonly-used libraries. These include:

- [BN.js](https://github.com/indutny/bn.js) (version `5.x`)
- [rlp](https://github.com/ethereumjs/rlp) (version `2.x`)

# EthereumJS

See our organizational [documentation](https://ethereumjs.readthedocs.io) for an introduction to `EthereumJS` as well as information on current standards and best practices.

If you want to join for work or do improvements on the libraries have a look at our [contribution guidelines](https://ethereumjs.readthedocs.io/en/latest/contributing.html).

# LICENSE

MPL-2.0
