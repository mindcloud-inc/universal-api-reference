# PDF to Excel with ComPDFKit PDF Editor

Creates a PDF-to-Excel conversion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/xlsx`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF to Excel](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
