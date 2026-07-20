# List Related Terms with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords-explorer/related-terms`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Related Terms](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-related-terms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `keywords` | query | `string` | yes | Seed keyword or comma-separated seed keywords. |
| `select` | query | `string` | yes | Comma-separated related-term columns to return. |
