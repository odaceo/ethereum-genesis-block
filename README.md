# Ethereum :: Genesis Block

[![License](https://img.shields.io/github/license/odaceo/ethereum-genesis-block.svg)](LICENSE)

## Description

This project aims to reference the genesis block of the Ethereum blockchain in JSON format for the following networks:

* [MainNet](mainnet.json)
* [TestNet (Ropsten)](testnet.json)
* [Rinkeby](rinkeby.json)
* [Görli](gorli.json)

## Code

Below the `Go` code used to dump the MainNet genesis block in JSON format:

```go
package main

import "io/ioutil"
import "github.com/ethereum/go-ethereum/core"

func check(e error) {
    if e != nil {
        panic(e)
    }
}

func main() {
    genesisBlock := core.DefaultGenesisBlock()
    bytes, _ := genesisBlock.MarshalJSON()
    err := ioutil.WriteFile("./mainnet.json", bytes, 0644)
    check(err)
}
```

## Reporting Issues

Issues can be reported at [https://github.com/odaceo/ethereum-genesis-block/issues](https://github.com/odaceo/ethereum-genesis-block/issues)

## Source code

The source code is available at [https://github.com/odaceo/ethereum-genesis-block](https://github.com/odaceo/ethereum-genesis-block)

## License

All the source code is distributed under [ASL 2.0](LICENSE).

## Copyright

© 2020 [Odaceo](https://odaceo.ch). All rights reserved.
