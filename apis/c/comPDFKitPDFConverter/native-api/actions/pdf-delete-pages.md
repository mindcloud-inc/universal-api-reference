# PDF Delete Pages with ComPDFKit PDF Converter

Creates a PDF with selected pages deleted.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/delete`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF Delete Pages](https://api.compdf.com/feature/pdf-editor-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
