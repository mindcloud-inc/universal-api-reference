# Search Google News with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/google/news`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [Search Google News](https://docs.piloterr.com/google-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gl` | query | `string` | no | Two-letter Google country code. |
| `hl` | query | `string` | no | Two-letter Google language code. |
| `page` | query | `string` | no | Results page number. |
| `query` | query | `string` | yes | Google News search query. |
