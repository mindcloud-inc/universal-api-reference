# Get Wallet Transfers with Chainstream

Retrieves wallet transfers from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/transfers`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet Transfers](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-transfers-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `cursor` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Number of results per page. |
| `direction` | query | `string` | no | Pagination direction (next or prev). |
| `tokenAddress` | query | `string` | no | An address of a token. |
| `fromTimestamp` | query | `number` | no | Filter transfers after this timestamp (Unix epoch seconds). |
| `toTimestamp` | query | `number` | no | Filter transfers before this timestamp (Unix epoch seconds). |
| `minTokenAmount` | query | `string` | no | Minimum token amount filter (inclusive). |
| `maxTokenAmount` | query | `string` | no | Maximum token amount filter (inclusive). |
| `minTokenAmountInUsd` | query | `string` | no | Minimum token amount in USD filter (inclusive). |
| `maxTokenAmountInUsd` | query | `string` | no | Maximum token amount in USD filter (inclusive). |
