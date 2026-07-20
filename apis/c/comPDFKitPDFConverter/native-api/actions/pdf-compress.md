# PDF Compress with ComPDFKit PDF Converter

Creates a compressed PDF from an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/compress`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Compress](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
