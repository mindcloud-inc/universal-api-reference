# Build DEX Route with Chainstream

Calculates the best DEX swap route in Chainstream.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/dex/:chain/route`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Build DEX Route](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-route-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks |
| `dex` | body | `string` | yes | DEX identifier for the trade |
| `userAddress` | body | `string` | yes | Public key of the wallet initiating the transaction |
| `priorityFee` | body | `string` | no | Priority fee to increase transaction processing speed |
| `amount` | body | `string` | yes | Amount to swap |
| `swapMode` | body | `string` | yes | Swap direction mode |
| `slippage` | body | `number` | yes | Slippage tolerance percentage |
| `inputMint` | body | `string` | no | Input token mint address |
| `outputMint` | body | `string` | no | Output token mint address |
| `recipientAddress` | body | `string` | no | Recipient wallet address for the swap |
| `permit` | body | `string` | no | Permit data for the swap |
| `deadline` | body | `number` | no | Swap deadline timestamp |
| `tipFee` | body | `string` | no | Tip fee to increase transaction processing speed |
| `isAntiMev` | body | `boolean` | no | Whether to enable anti-MEV protection |
| `maxFeePerGas` | body | `string` | no | Maximum fee per gas unit in wei |
| `maxPriorityFeePerGas` | body | `string` | no | Maximum priority fee per gas unit in wei |
| `gasPrice` | body | `string` | no | Gas price in wei |
| `gasLimit` | body | `string` | no | Gas limit for the transaction |
