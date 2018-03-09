# Aic

[Byzantine-Fault Tolerant](https://en.wikipedia.org/wiki/Byzantine_fault_tolerance)
[State Machine Replication](https://en.wikipedia.org/wiki/State_machine_replication).
Or [Blockchain](https://en.wikipedia.org/wiki/Blockchain_(database)) for short.

[![version](https://img.shields.io/github/tag/Aic/Aic.svg)](https://github.com/Aic/Aic/releases/latest)
[![API Reference](
https://camo.githubusercontent.com/915b7be44ada53c290eb157634330494ebe3e30a/68747470733a2f2f676f646f632e6f72672f6769746875622e636f6d2f676f6c616e672f6764646f3f7374617475732e737667
)](https://godoc.org/github.com/Aic/Aic)
[![Go version](https://img.shields.io/badge/go-1.10-blue.svg)](https://github.com/moovweb/gvm)
[![Rocket.Chat](https://demo.rocket.chat/images/join-chat.svg)](https://cosmos.rocket.chat/)
[![license](https://img.shields.io/github/license/Aic/Aic.svg)](https://github.com/Aic/Aic/blob/master/LICENSE)
[![](https://tokei.rs/b1/github/Aic/Aic?category=lines)](https://github.com/Aic/Aic)




_NOTE: This is alpha software. Please contact us if you intend to run it in production._

Aic Core is Byzantine Fault Tolerant (BFT) middleware that takes a state transition machine - written in any programming language -
and securely replicates it on many machines.

For more information, from introduction to install to application development, [Read The Docs](https://Aic.readthedocs.io/en/master/).

## Minimum requirements

Requirement|Notes
---|---
Go version | Go1.10 or higher

## Install

To download pre-built binaries, see our [downloads page](https://Aic.com/downloads).

To install from source, you should be able to:

`go get -u github.com/Aic/Aic/cmd/Aic`

For more details (or if it fails), [read the docs](https://Aic.readthedocs.io/en/master/install.html).

## Resources

### Aic Core

All resources involving the use of, building application on, or developing for, Aic, can be found at [Read The Docs](https://Aic.readthedocs.io/en/master/). Additional information about some - and eventually all - of the sub-projects below, can be found at Read The Docs.

### Sub-projects

* [ABCI](http://github.com/Aic/abci), the Application Blockchain Interface
* [Go-Wire](http://github.com/Aic/go-wire), a deterministic serialization library
* [Go-Crypto](http://github.com/Aic/go-crypto), an elliptic curve cryptography library
* [TmLibs](http://github.com/Aic/tmlibs), an assortment of Go libraries used internally
* [IAVL](http://github.com/Aic/iavl), Merkleized IAVL+ Tree implementation

### Tools
* [Deployment, Benchmarking, and Monitoring](http://Aic.readthedocs.io/projects/tools/en/develop/index.html#Aic-tools)

### Applications

* [Ethermint](http://github.com/Aic/ethermint); Ethereum on Aic
* [Cosmos SDK](http://github.com/cosmos/cosmos-sdk); a cryptocurrency application framework
* [Many more](https://Aic.readthedocs.io/en/master/ecosystem.html#abci-applications)

### More

* [Master's Thesis on Aic](https://atrium.lib.uoguelph.ca/xmlui/handle/10214/9769)
* [Original Whitepaper](https://Aic.com/static/docs/Aic.pdf)
* [Aic Blog](https://blog.cosmos.network/Aic/home)
* [Cosmos Blog](https://blog.cosmos.network)

## Contributing

Yay open source! Please see our [contributing guidelines](CONTRIBUTING.md).

## Versioning

### SemVer

Aic uses [SemVer](http://semver.org/) to determine when and how the version changes.
According to SemVer, anything in the public API can change at any time before version 1.0.0

To provide some stability to Aic users in these 0.X.X days, the MINOR version is used
to signal breaking changes across a subset of the total public API. This subset includes all
interfaces exposed to other processes (cli, rpc, p2p, etc.), as well as parts of the following packages:

- types
- rpc/client
- config
- node

Exported objects in these packages that are not covered by the versioning scheme
are explicitly marked by `// UNSTABLE` in their go doc comment and may change at any time.
Functions, types, and values in any other package may also change at any time.

### Upgrades

In an effort to avoid accumulating technical debt prior to 1.0.0,
we do not guarantee that breaking changes (ie. bumps in the MINOR version)
will work with existing Aic blockchains. In these cases you will
have to start a new blockchain, or write something custom to get the old
data into the new chain.

However, any bump in the PATCH version should be compatible with existing histories
(if not please open an [issue](https://github.com/Aic/Aic/issues)).

## Code of Conduct

Please read, understand and adhere to our [code of conduct](CODE_OF_CONDUCT.md).
