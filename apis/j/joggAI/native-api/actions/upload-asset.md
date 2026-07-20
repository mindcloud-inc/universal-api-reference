# Upload Asset with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/upload/asset`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Upload Asset](https://docs.jogg.ai/api-reference/v2/Asset/UploadAsset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | body | `string` | yes | MIME type of the file |
| `file_size` | body | `number` | no | File size in bytes |
| `filename` | body | `string` | yes | Name of the file to upload |
