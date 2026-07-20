# PDF Content Compare with ComPDFKit PDF Converter

Creates a content comparison for two PDFs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/contentCompare`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Content Compare](https://api.compdf.com/feature/pdf-editor-api)

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
