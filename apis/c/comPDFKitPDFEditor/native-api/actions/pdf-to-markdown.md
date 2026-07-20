# PDF to Markdown with ComPDFKit PDF Editor

Creates a PDF-to-Markdown conversion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/markdown`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF to Markdown](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
