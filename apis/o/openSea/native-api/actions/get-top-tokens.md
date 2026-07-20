# Get Top Tokens with OpenSea

Retrieves top tokens from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tokens/top`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Top Tokens](https://docs.opensea.io/reference/get_top_tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of results to return (default: 20, max: 100) |
| `chains[]` | query | `array<string>` | no | Filter by blockchain(s) Send multiple values as a string separated by `,`. |
| `chains[]` | query | `array<string>` | no | Filter by blockchain(s) Send multiple values as a string separated by `,`. |
| `cursor` | query | `string` | no | Pagination cursor for next page |
