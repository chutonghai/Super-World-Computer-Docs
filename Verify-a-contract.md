# Verify a contract
This guide will help you verify a smart contract on Taiko.

## Prerequisites

You have a contract deployed on Taiko and the source code available.

## Mainnet


### Verify a contract with Foundry 

Replace the contract address and filepath to contract below, and then execute in terminal to verify your contract.

```bash
forge verify-contract 0x526317252e346978869d178081dA2cd10ac8b56D src/Counter.sol:Counter \
  --verifier-url https://blockscoutapi.mainnet.taiko.xyz/api\? \
  --verifier blockscout
```

It's also possible to verify the contract through `Taikoscan` API as follows:

```bash
forge verify-contract 0x526317252e346978869d178081dA2cd10ac8b56D src/Counter.sol:Counter \
  --watch \
  --verifier-url https://api.taikoscan.io/api \
  --etherscan-api-key {YOUR_API_KEY} 
```

## Hekla


### Verify a contract with Foundry

Replace the contract address and filepath to contract below, and then execute in terminal to verify your contract.

```bash
forge verify-contract 0x526317252e346978869d178081dA2cd10ac8b56D src/Counter.sol:Counter \
  --verifier-url https://blockscoutapi.hekla.taiko.xyz/api\? \
  --verifier blockscout
```

>For some users the above command does not work on Blockscout (currently investigating). You can also try passing a different `--verifier-url`:

```bash "https://blockscoutapi.hekla.taiko.xyz/api?module=contract&action=verify"
--verifier-url https://blockscoutapi.hekla.taiko.xyz/api?module=contract&action=verify
```

### Verify a contract with Hardhat or other alternatives

Check out the Blockscout docs [here](https://docs.blockscout.com/for-users/verifying-a-smart-contract)!