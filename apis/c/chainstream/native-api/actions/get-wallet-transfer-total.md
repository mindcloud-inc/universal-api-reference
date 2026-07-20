# Get Wallet Transfer Total with Chainstream

Retrieves wallet transfer totals from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/transfer-total`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet Transfer Total](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-transfer-total-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `tokenAddress` | query | `string` | no | An address of a token. |
| `fromTimestamp` | query | `number` | no | Filter transfers after this timestamp (Unix epoch seconds). |
| `toTimestamp` | query | `number` | no | Filter transfers before this timestamp (Unix epoch seconds). |
| `minTokenAmount` | query | `string` | no | Minimum token amount filter (inclusive). |
| `maxTokenAmount` | query | `string` | no | Maximum token amount filter (inclusive). |
| `minTokenAmountInUsd` | query | `string` | no | Minimum token amount in USD filter (inclusive). |
| `maxTokenAmountInUsd` | query | `string` | no | Maximum token amount in USD filter (inclusive). |
