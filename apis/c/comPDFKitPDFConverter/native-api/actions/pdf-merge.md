# PDF Merge with ComPDFKit PDF Converter

Creates a merged PDF from multiple files.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/merge`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Merge](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
