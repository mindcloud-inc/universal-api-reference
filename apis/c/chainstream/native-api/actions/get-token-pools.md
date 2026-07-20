# Get Token Pools with Chainstream

Retrieves token pools from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/:tokenAddress/pools`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Token Pools](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-tokenaddress-pools-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `tokenAddress` | path | `string` | yes | Token contract address |
| `cursor` | query | `string` | no | Pagination cursor |
| `limit` | query | `string` | no | Number of results per page |
| `direction` | query | `string` | no | Pagination direction |
| `sortBy` | query | `string` | no | Pool sort field |
| `sortDirection` | query | `string` | no | Sort direction |
| `minTvlInSol` | query | `string` | no | Minimum TVL in SOL |
| `maxTvlInSol` | query | `string` | no | Maximum TVL in SOL |
| `minTvlInUsd` | query | `string` | no | Minimum TVL in USD |
| `maxTvlInUsd` | query | `string` | no | Maximum TVL in USD |
