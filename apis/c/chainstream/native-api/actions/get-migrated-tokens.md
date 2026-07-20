# Get Migrated Tokens with Chainstream

Retrieves migrated tokens from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ranking/:chain/migrated`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Migrated Tokens](https://docs.chainstream.io/en/api-reference/endpoint/data/ranking/v2/ranking-chain-migrated-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `sortBy` | query | `string` | no | Sort field. |
| `sortDirection` | query | `string` | no | Sort direction. |
| `tag` | query | `string` | no | Ranking tag filter. |
