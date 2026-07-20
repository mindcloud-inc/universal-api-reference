# Create Waveform with RemasterMedia

Creates a waveform mediafile in RemasterMedia.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/process`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Create Waveform](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | yes | ID of the mediafile to use as waveform source. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when processing finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the derived mediafile. |
