# Complete External Upload with Discourse

Completes an external upload in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/complete-external-upload.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Complete External Upload](https://docs.discourse.org/#tag/Uploads/operation/completeExternalUpload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `for_private_message` | body | `string` | no | Whether the upload is for a private message. Accepted values: `0`, `1`. |
| `for_site_setting` | body | `string` | no | Whether the upload is for a site setting. Accepted values: `0`, `1`. |
| `pasted` | body | `string` | no | Whether the upload was pasted into the composer. Accepted values: `0`, `1`. |
| `unique_identifier` | body | `string` | yes | The unique identifier returned by Generate Presigned Put. |
