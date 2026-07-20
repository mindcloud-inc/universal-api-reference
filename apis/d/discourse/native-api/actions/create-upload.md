# Create Upload with Discourse

Creates a new upload in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Upload](https://docs.discourse.org/#tag/Uploads/operation/createUpload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Binary file payload for the multipart upload. |
| `synchronous` | body | `boolean` | no | Whether to return an upload id and URL immediately. |
| `type` | body | `string` | yes | Upload type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `user_id` | body | `number` | no | Required when uploading an avatar. |
