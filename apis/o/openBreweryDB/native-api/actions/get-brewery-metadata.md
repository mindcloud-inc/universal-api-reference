# Get Brewery Metadata with Open Brewery DB

Retrieves brewery metadata from Open Brewery DB.

## Endpoint

- **Method:** `GET`
- **Path:** `/breweries/meta`
- **Base URL:** `https://api.openbrewerydb.org/v1`
- **Official documentation:** [Get Brewery Metadata](https://www.openbrewerydb.org/documentation#metadata)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by_city` | query | `string` | no | Filter brewery metadata by city. Use underscores or URL encoding for spaces. |
| `by_country` | query | `string` | no | Filter brewery metadata by country. Use underscores or URL encoding for spaces. |
| `by_name` | query | `string` | no | Filter brewery metadata by name. Use underscores or URL encoding for spaces. |
| `by_state` | query | `string` | no | Filter brewery metadata by full state name; abbreviations are not supported. |
| `by_postal` | query | `string` | no | Filter brewery metadata by postal or ZIP code. Postal+4 may use a hyphen or underscore. |
| `by_type` | query | `list` | no | Filter metadata by brewery type: micro, nano, regional, brewpub, large, planning, bar, contract, proprietor, or closed. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `by_dist` | query | `string` | no | Sort/filter metadata by distance from an origin point in latitude,longitude format. |
| `by_ids` | query | `string` | no | Comma-separated list of brewery IDs for metadata filtering. Send multiple values as a string separated by `,`. |
