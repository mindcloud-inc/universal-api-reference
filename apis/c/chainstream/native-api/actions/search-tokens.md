# Search Tokens with Chainstream

Finds tokens in Chainstream by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/token/search`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Search Tokens](https://docs.chainstream.io/en/api-reference/endpoint/data/token/v2/token-search-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chains` | query | `string` | no | Chain filter |
| `cursor` | query | `string` | no | Pagination cursor |
| `direction` | query | `string` | no | Pagination direction |
| `limit` | query | `string` | no | Number of results per page |
| `mode` | query | `string` | no | Search mode |
| `protocols` | query | `string` | no | Protocol filter |
| `q` | query | `string` | no | Search query string for token name, symbol, or address |
| `sort` | query | `string` | no | Sort direction |
| `sortBy` | query | `string` | no | Field to sort by |
