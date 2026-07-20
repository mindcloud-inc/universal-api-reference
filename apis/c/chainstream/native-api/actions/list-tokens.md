# List Tokens with Chainstream

Retrieves tokens for a blockchain from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/:chain/list`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [List Tokens](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-chain-list-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | Supported blockchain chain |
| `cursor` | query | `string` | no | Pagination cursor |
| `direction` | query | `string` | no | Pagination direction |
| `limit` | query | `string` | no | Number of results per page |
| `sort` | query | `string` | no | Sort direction |
| `sortBy` | query | `string` | no | Sort by field |
