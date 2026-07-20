# List Derived Mediafiles with RemasterMedia

Retrieves derived mediafiles from RemasterMedia.

## Endpoint

- **Method:** `GET`
- **Path:** `/mediafile/{{id}}/derived`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [List Derived Mediafiles](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-derived-mediafiles-get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the mediafile whose derived mediafiles should be listed. |
