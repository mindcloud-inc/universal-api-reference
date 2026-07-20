# Create Mediafile with RemasterMedia

Creates a mediafile in RemasterMedia.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/create`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Create Mediafile](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-create-new-mediafile-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_url` | body | `string` | yes | URL of the source audio or video file to submit. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when media analysis finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the mediafile. |
