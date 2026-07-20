# Upload File From URL Or Base64 with Docsumo

Uploads a document to Docsumo from a URL or Base64.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/eevee/apikey/upload/custom/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Upload File From URL Or Base64](https://support.docsumo.com/reference/api-v1-upload-custom)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_base64` | body | `string` | no | Base64-encoded file content. |
| `file_name` | body | `string` | no | File name to use with base64 uploads. |
| `file_url` | body | `string` | no | Public URL of the file to upload. |
| `type` | body | `string` | yes | Internal document type for the uploaded file. |
