# Upload File in Chunks with Grok

Uploads file chunks to an existing Grok upload.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files:uploadChunks`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Upload File in Chunks](https://docs.x.ai/developers/rest-api-reference/files/upload#upload-a-file-in-chunks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | File identifier to upload chunks into. |
| `chunk` | body | `string` | yes | File data chunk payload. |
