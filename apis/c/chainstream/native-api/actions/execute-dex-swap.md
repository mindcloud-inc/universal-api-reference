# Execute DEX Swap with Chainstream

Creates a DEX swap transaction in Chainstream.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/dex/:chain/swap`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Execute DEX Swap](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-swap-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks |
| `dex` | body | `string` | yes | DEX identifier for the trade |
| `userAddress` | body | `string` | yes | Public key of the wallet initiating the transaction |
| `priorityFee` | body | `string` | no | Priority fee to increase transaction processing speed |
| `poolAddress` | body | `string` | no | DEX pool address |
| `amount` | body | `string` | yes | Amount to swap |
| `swapMode` | body | `string` | yes | Swap direction mode |
| `slippage` | body | `number` | yes | Slippage tolerance percentage |
| `inputMint` | body | `string` | no | Input token mint address |
| `outputMint` | body | `string` | no | Output token mint address |
