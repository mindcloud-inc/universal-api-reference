# Upload File from URL with PDF.co

Uploads a file from a URL to PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/upload/url`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Upload File from URL](https://docs.pdf.co/api-reference/file-upload/upload-url-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the file to upload. |
| `name` | body | `string` | no | Optional name for the stored temporary file. |
| `expiration` | body | `number` | no | Optional temporary file expiration in minutes. |
