# Create Blob with Modelry

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/blobs`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Create Blob](https://files.cgtarsenal.com/api/doc/index.html#api-Uploads-Blobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blob.filename` | body | `string` | yes | Filename for the blob. |
| `blob.byte_size` | body | `number` | yes | File size in bytes. |
| `blob.checksum` | body | `string` | yes | Base64-encoded MD5 checksum. |
| `blob.content_type` | body | `string` | yes | File content type. |
