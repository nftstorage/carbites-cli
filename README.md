# carbites-cli

[![Build](https://github.com/nftstorage/carbites-cli/actions/workflows/main.yml/badge.svg)](https://github.com/nftstorage/carbites-cli/actions/workflows/main.yml)
[![dependencies Status](https://status.david-dm.org/gh/nftstorage/carbites-cli.svg)](https://david-dm.org/nftstorage/carbites-cli)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

CLI tool for splitting a single CAR into multiple CARs from the comfort of your terminal.

## Install
Make sure you have installed Node.js higher than v15.0.0.

```sh
npm install -g carbites-cli
```

## Usage

```sh
# Split a big CAR into many smaller CARs
carbites split big.car --size 100MB --strategy simple # (default size & strategy)

# Join many split CARs back into a single CAR.
carbites join big-0.car big-1.car ...
# Note: not a tool for joining arbitrary CARs together! The split CARs MUST
# belong to the same CAR and big-0.car should be the first argument.

# If you are looking to split a CAR to fit under the NFT.Storage 100MB limit using the HTTP API, use:
carbites split example.car --size 10MB --strategy treewalk
```

## Contribute

Feel free to dive in! [Open an issue](https://github.com/nftstorage/carbites-cli/issues/new) or submit PRs.

## License

Dual-licensed under [MIT](https://github.com/nftstorage/carbites-cli/blob/main/LICENSE-MIT) + [Apache 2.0](https://github.com/nftstorage/carbites-cli/blob/main/LICENSE-APACHE)
