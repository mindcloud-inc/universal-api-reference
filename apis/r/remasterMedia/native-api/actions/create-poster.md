# Create Poster with RemasterMedia

Creates a poster mediafile in RemasterMedia.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/process`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Create Poster](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | yes | ID of the mediafile to use as poster source. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when processing finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the derived mediafile. |
