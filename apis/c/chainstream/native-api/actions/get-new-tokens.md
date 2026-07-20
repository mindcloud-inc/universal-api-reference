# Get New Tokens with Chainstream

Retrieves new tokens from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ranking/:chain/newTokens`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get New Tokens](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-newtokens-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `sortBy` | query | `string` | no | Sort field. |
| `sortDirection` | query | `string` | no | Sort direction. |
| `tag` | query | `string` | no | Ranking tag filter. |
