# Get Top Collections with OpenSea

Retrieves top collections from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/collections/top`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Top Collections](https://docs.opensea.io/reference/get_top_collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort_by` | query | `string` | no | The stat to sort collections by (always sorted descending). Options: one_day_volume, seven_days_volume, thirty_days_volume, floor_price, one_day_sales, seven_days_sales, thirty_days_sales, total_volume, total_sales |
| `chains[]` | query | `array<string>` | no | Blockchain(s) to filter by. Comma-separated list of chain identifiers. Unsupported chains are silently ignored; a 400 is returned only if all specified chains are unsupported. Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Category to filter by (e.g. art, gaming, memberships, music, pfps, photography, domain-names, virtual-worlds, sports-collectibles). |
| `limit` | query | `number` | no | Maximum number of collections to return (1-100). |
| `cursor` | query | `string` | no | Cursor for pagination |
