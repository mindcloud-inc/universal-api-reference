# Add Files In Folder with Docsumo

Uploads a document into a specific Docsumo folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/eevee/documents/upload/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Add Files In Folder](https://support.docsumo.com/reference/post_api-v1-eevee-documents-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Binary file payload for multipart upload. |
| `folder_id` | body | `string` | yes | Folder ID that should receive the uploaded files. |
| `type` | body | `string` | yes | Internal document type for uploaded files. |
