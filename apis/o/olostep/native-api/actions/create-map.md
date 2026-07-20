# Create Map with Olostep

Creates a new map in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/maps`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create Map](https://docs.olostep.com/api-reference/maps/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The website URL to map. |
| `search_query` | body | `string` | no | Optional search query to sort map URLs by relevance. |
| `top_n` | body | `number` | no | Optional number of top URLs to return for a search query. |
| `include_subdomain` | body | `boolean` | no | Whether to include subdomains of the given URL. |
| `include_urls[]` | body | `array<string>` | no | Optional glob patterns of URL paths to include. Send multiple values as a array. |
| `exclude_urls[]` | body | `array<string>` | no | Optional glob patterns of URL paths to exclude. Send multiple values as a array. |
| `cursor` | body | `string` | no | Optional pagination cursor from a previous map response. |
