# PDF Extract Page with ComPDFKit PDF Editor

Creates a PDF page extraction task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/extract`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF Extract Page](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
