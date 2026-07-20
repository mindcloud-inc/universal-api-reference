# Get SERP Overview with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/serp-overview/serp-overview`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get SERP Overview](https://docs.ahrefs.com/en/api/reference/serp-overview/get-serp-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword to return SERP overview for. |
| `top_positions` | query | `string` | no | Number of top organic SERP positions to return. |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `select` | query | `string` | yes | Comma-separated SERP columns to return. |
