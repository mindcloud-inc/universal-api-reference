# Search Google Images with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/google/images`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [Search Google Images](https://docs.piloterr.com/google-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gl` | query | `string` | no | Two-letter Google country code. |
| `hl` | query | `string` | no | Two-letter Google language code. |
| `page` | query | `string` | no | Results page number. |
| `query` | query | `string` | yes | Google Images search query. |
