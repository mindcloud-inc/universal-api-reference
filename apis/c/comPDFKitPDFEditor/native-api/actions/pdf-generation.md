# PDF Generation with ComPDFKit PDF Editor

Creates a PDF generation task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/generate`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF Generation](https://api.compdf.com/api-reference/pdf-generate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
