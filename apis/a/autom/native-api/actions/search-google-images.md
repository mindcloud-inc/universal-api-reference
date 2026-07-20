# Search Google Images with Autom

Finds Google image results in Autom.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/google/images`
- **Base URL:** `https://api.autom.dev`
- **Official documentation:** [Search Google Images](https://docs.autom.dev/google-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The image search query to run. |
| `gl` | query | `string` | no | Two-letter Google country code such as us, uk, or fr. |
| `hl` | query | `string` | no | Two-letter Google language code such as en, es, or fr. |
| `page` | query | `number` | no | Result page number to request. |
