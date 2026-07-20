# Create Multipart Upload with Discourse

Creates a multipart upload in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/create-multipart.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Multipart Upload](https://docs.discourse.org/#tag/Uploads/operation/createMultipartUpload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename for the multipart upload. |
| `file_size` | body | `number` | yes | File size in bytes. |
| `upload_type` | body | `string` | yes | Upload type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
