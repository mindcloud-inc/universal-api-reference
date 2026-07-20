# Process Mediafile with RemasterMedia

Processes a mediafile in RemasterMedia with action-specific options.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/process`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Process Mediafile](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | yes | ID of the mediafile to process. |
| `action` | body | `string` | yes | Process action to perform, such as remaster, waveform, poster, or denoise. |
| `options` | body | `object` | no | Action-specific options object. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when processing finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the derived mediafile. |
