## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
### Traceback of commands
1. Sending some wei to my address in the default keystore (from the anvil's default account):
`cast send 0x09a6e8987Ca4824F557EED4Bfb48C7560912bd5F --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80 --value 999999999999999`

2. The contracts created on anvil at the address 0xEf20890878a349f8ff1158247569b8593d3acb46.
It should repeatedly use the same address in deterministic manner, right?

3. I am building a transaction but not sending it yet: `cast mktx $COUNTER_ADDR "setNumber(uint256)" 88`

## Progress
[x] Look, how to deploy the existing conracts onto the Sepolia
[] I've deployed the fund me contract on sepolia. I now need to modify the fundMe contract with a different price feed (Pyth) and then have a function to get the price or update
the price. And then redeploy!

