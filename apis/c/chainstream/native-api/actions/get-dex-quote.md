# Get DEX Quote with Chainstream

Retrieves a DEX quote from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/dex/:chain/quote`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get DEX Quote](https://docs.chainstream.io/en/api-reference/endpoint/defi/dex/v2/dex-chain-quote-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks |
| `dex` | query | `string` | yes | DEX identifier |
| `amount` | query | `string` | yes | Amount to quote |
| `inputMint` | query | `string` | yes | Input token mint address |
| `outputMint` | query | `string` | yes | Output token mint address |
| `exactIn` | query | `boolean` | yes | Whether the amount is exact input |
| `slippage` | query | `number` | yes | Slippage tolerance percentage |
