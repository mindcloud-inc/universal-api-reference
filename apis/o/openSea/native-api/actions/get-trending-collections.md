# Get Trending Collections with OpenSea

Retrieves trending collections from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/collections/trending`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Trending Collections](https://docs.opensea.io/reference/get_trending_collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeframe` | query | `string` | no | Time window for trending calculation. Options: one_minute, five_minutes, fifteen_minutes, one_hour, one_day, seven_days, thirty_days, one_year, all_time. |
| `chains[]` | query | `array<string>` | no | Blockchain(s) to filter by. Comma-separated list of chain identifiers. Unsupported chains are silently ignored; a 400 is returned only if all specified chains are unsupported. Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Category to filter by (e.g. art, gaming, memberships, music, pfps, photography, domain-names, virtual-worlds, sports-collectibles). |
| `limit` | query | `number` | no | Maximum number of collections to return (1-100). |
| `cursor` | query | `string` | no | Cursor for pagination. Use the 'next' value from a previous response. |
