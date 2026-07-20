# Search Google News with Autom

Finds Google news results in Autom.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/google/news`
- **Base URL:** `https://api.autom.dev`
- **Official documentation:** [Search Google News](https://docs.autom.dev/google-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The news query to run. |
| `gl` | query | `string` | no | Two-letter Google country code such as us, uk, or fr. |
| `hl` | query | `string` | no | Two-letter Google language code such as en, es, or fr. |
| `page` | query | `number` | no | Result page number to request. |
