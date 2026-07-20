# PDF Split with ComPDFKit PDF Converter

Creates split PDF files from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/split`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Split](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
