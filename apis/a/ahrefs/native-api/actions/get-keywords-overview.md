# Get Keywords Overview with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords-explorer/overview`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Keywords Overview](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `keywords` | query | `string` | yes | Comma-separated keywords to show metrics for. |
| `select` | query | `string` | yes | Comma-separated keyword metric columns to return. |
