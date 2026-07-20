# Upload File with Docsumo

Uploads a document file to Docsumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/eevee/apikey/upload/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Upload File](https://support.docsumo.com/reference/api-v1-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Binary file payload for multipart upload. |
| `type` | body | `string` | yes | Internal document type for the uploaded file. |
