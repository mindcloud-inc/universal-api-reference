# Create Remaster with RemasterMedia

Creates a remastered mediafile in RemasterMedia.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/process`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Create Remaster](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | yes | ID of the mediafile to remaster. |
| `options.preset` | body | `string` | yes | Remastering preset name. |
| `options.offset` | body | `number` | no | Optional number of seconds to skip from the start. |
| `options.duration` | body | `number` | no | Optional output duration limit in seconds. |
| `options.html5_compatible` | body | `boolean` | no | Whether to create HTML5-compatible output. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when processing finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the derived mediafile. |
