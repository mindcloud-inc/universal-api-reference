# List Matching Terms with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords-explorer/matching-terms`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Matching Terms](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-matching-terms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `match_mode` | query | `string` | no | Keyword ideas match mode: terms or phrase. |
| `terms` | query | `string` | no | Use all keyword ideas or questions. |
| `keywords` | query | `string` | yes | Seed keyword or comma-separated seed keywords. |
| `select` | query | `string` | yes | Comma-separated matching-term columns to return. |
