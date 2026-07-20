# Upload File with Modelry

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/uploads`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Upload File](https://files.cgtarsenal.com/api/doc/index.html#api-Uploads-UploadFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Filename for the upload. |
| `base64_file` | body | `string` | yes | Base64-encoded file data. |
| `content_type` | body | `string` | yes | File content type. |
