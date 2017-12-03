# go-solidity-sha3

> Generate Solidity SHA3 (Keccak256) hashes in Go.

This package is the Go equivalent of `require('ethereumjs-abi').soliditySHA3` [NPM module](https://www.npmjs.com/package/ethereumjs-abi).

<!--
var a = new BN("0x12459c951127e0c374ff9105dda097662a027093", 16)

var s4 = abi.soliditySHA3(['address', 'uint256'], [a, new BN('200000000000000', 10)])

		// basic test
		hash := SoliditySHA3(
			Address("0x12459c951127e0c374ff9105dda097662a027093"),
			Uint256(200000000000000),
		)

		expected := "abb858e5d39c237b0c47db82052cdb7f933419e3c1d334c7c2558eb8c03734fc"
		if got := hex.EncodeToString(hash); got != expected {
-->

# Usage

Simple example

```go
package main

import (
	"encoding/hex"
	"fmt"
	"github.com/miguelmota/go-solidity-sha3"
)

func main() {
  hash := solsha3.SoliditySHA3(
    solsha3.Address("0x12459c951127e0c374ff9105dda097662a027093"),
    solsha3.Uint256(100),
    solsha3.String("foo"),
    solsha3.Bytes32("bar"),
    solsha3.Bool(true),
  )

  fmt.Println(hex.EncodeToString(hash))
}
```

Output

```bash
417a4c44724701ba79bb363151dff48909bc058a2c75a81e9cf5208ae4699369
```

# License

MIT
