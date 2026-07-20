# List Mediafiles with RemasterMedia

Retrieves mediafiles from RemasterMedia.

## Endpoint

- **Method:** `GET`
- **Path:** `/mediafiles`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [List Mediafiles](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-mediafiles-collection-get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | Beginning of time range as RFC3339. |
| `to` | query | `date` | yes | End of time range as RFC3339. |
| `page` | query | `number` | no | Page number. Defaults to 1. |
