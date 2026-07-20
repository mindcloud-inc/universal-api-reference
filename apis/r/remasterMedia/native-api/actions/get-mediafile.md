# Get Mediafile with RemasterMedia

Retrieves mediafile details from RemasterMedia.

## Endpoint

- **Method:** `GET`
- **Path:** `/mediafiles/{{id}}`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Get Mediafile](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-mediafile-details-get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the mediafile. |
