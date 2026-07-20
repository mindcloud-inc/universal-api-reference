# PDF Cover Compare with ComPDFKit PDF Converter

Creates a cover comparison for two PDFs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/coverCompare`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Cover Compare](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `file` | body | `file` | yes |
