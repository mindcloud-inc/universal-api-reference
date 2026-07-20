# Get Keyword Volume History with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords-explorer/volume-history`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Keyword Volume History](https://docs.ahrefs.com/en/api/reference/keywords-explorer/get-volume-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `keyword` | query | `string` | yes | Comma-separated keywords to show volume history for. |
