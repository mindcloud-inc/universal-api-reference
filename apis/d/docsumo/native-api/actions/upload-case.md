# Upload Case with Docsumo

Creates or updates a Docsumo case and uploads files.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/upload-service/agents/casetype/case`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Upload Case](https://support.docsumo.com/reference/upload-case)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `casetype_id` | body | `string` | yes | Case type identifier to upload into. |
| `file` | body | `string` | no | Binary file payload for multipart upload. |
| `file_base64` | body | `string` | no | Base64-encoded file content for case upload. |
| `file_url` | body | `string` | no | Public URL of the file to upload into the case. |
