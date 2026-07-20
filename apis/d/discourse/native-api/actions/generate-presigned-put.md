# Generate Presigned Put with Discourse

Generates a presigned upload URL in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/generate-presigned-put.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Generate Presigned Put](https://docs.discourse.org/#tag/Uploads/operation/generatePresignedPut)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename for the direct upload. |
| `file_size` | body | `number` | yes | File size in bytes. |
| `type` | body | `string` | yes | Upload type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
