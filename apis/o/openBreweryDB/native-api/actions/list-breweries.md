# List Breweries with Open Brewery DB

Retrieves breweries from Open Brewery DB.

## Endpoint

- **Method:** `GET`
- **Path:** `/breweries`
- **Base URL:** `https://api.openbrewerydb.org/v1`
- **Official documentation:** [List Breweries](https://www.openbrewerydb.org/documentation#list-breweries)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by_city` | query | `string` | no | Filter breweries by city. Use underscores or URL encoding for spaces. |
| `by_country` | query | `string` | no | Filter breweries by country. Use underscores or URL encoding for spaces. |
| `by_name` | query | `string` | no | Filter breweries by name. Use underscores or URL encoding for spaces. |
| `by_state` | query | `string` | no | Filter breweries by full state name; abbreviations are not supported. |
| `by_postal` | query | `string` | no | Filter breweries by postal or ZIP code. Postal+4 may use a hyphen or underscore. |
| `by_type` | query | `list` | no | Filter by brewery type: micro, nano, regional, brewpub, large, planning, bar, contract, proprietor, or closed. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `by_dist` | query | `string` | no | Sort by distance from an origin point in latitude,longitude format. Do not combine with sort. |
| `by_ids` | query | `string` | no | Comma-separated list of brewery IDs. Send multiple values as a string separated by `,`. |
