# Get Drops with OpenSea

Retrieves drops from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/drops`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Drops](https://docs.opensea.io/reference/get_drops)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Drop calendar type: featured, upcoming, or recently_minted |
| `limit` | query | `number` | no | Number of results to return (1-100, default: 20) |
| `chains[]` | query | `array<string>` | no | Comma-separated list of chains to filter by (e.g. ethereum, base). Omit to return drops on all chains. Send multiple values as a string separated by `,`. |
| `cursor` | query | `string` | no | Pagination cursor for next page |
