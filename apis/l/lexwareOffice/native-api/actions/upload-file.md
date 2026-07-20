# Upload File with Lexware Office

Uploads a bookkeeping voucher file to Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Upload File](https://developers.lexware.io/docs/#files-endpoint-upload-a-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF, image, or XML file content to upload. |
