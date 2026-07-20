# Upload File Using Base64 with PDF.co

Uploads a file from Base64 to PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/upload/base64`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Upload File Using Base64](https://docs.pdf.co/api-reference/file-upload/upload-base64)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Base64-encoded file content. |
| `name` | body | `string` | no | Filename to use for uploaded content. |
| `expiration` | body | `number` | no | Optional temporary file expiration in minutes. |
