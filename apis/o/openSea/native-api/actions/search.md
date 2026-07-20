# Search OpenSea with OpenSea

Finds items in OpenSea by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/search`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Search OpenSea](https://docs.opensea.io/reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text |
| `chains[]` | query | `array<string>` | no | Filter by blockchain(s) Send multiple values as a string separated by `,`. |
| `asset_types[]` | query | `array<string>` | no | Filter by asset type(s). Valid values: collection, nft, token, account. Defaults to [collection, token] if not specified. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Number of results to return (default: 20, max: 50) |
