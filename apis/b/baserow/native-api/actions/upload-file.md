# Upload File with Baserow

Uploads a file directly to Baserow.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/user-files/upload-file/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Upload File](https://api.baserow.io/api/redoc/#operation/upload_file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file contents to upload. |
