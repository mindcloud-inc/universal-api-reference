# Get Source Mediafile with RemasterMedia

Retrieves the source mediafile from RemasterMedia.

## Endpoint

- **Method:** `GET`
- **Path:** `/mediafile/{{id}}/source`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Get Source Mediafile](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-source-mediafile-get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the mediafile. |
