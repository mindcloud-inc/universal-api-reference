# PDF Rotate Pages with ComPDFKit PDF Converter

Creates a PDF with rotated pages.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/rotation`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Rotate Pages](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
