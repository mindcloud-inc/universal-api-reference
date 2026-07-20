# Search Google with Autom

Finds Google search results in Autom.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/google/search`
- **Base URL:** `https://api.autom.dev`
- **Official documentation:** [Search Google](https://docs.autom.dev/google-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The Google search query to run. |
| `gl` | query | `string` | no | Two-letter Google country code such as us, uk, or fr. |
| `hl` | query | `string` | no | Two-letter Google language code such as en, es, or fr. |
| `page` | query | `number` | no | Result page number to request. |
