# Search Google with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/google/search`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [Search Google](https://docs.piloterr.com/google-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gl` | query | `string` | no | Two-letter Google country code. |
| `hl` | query | `string` | no | Two-letter Google language code. |
| `query` | query | `string` | yes | Google search query. |
