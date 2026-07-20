# PDF to Markdown with ComPDFKit PDF Converter

Creates a Markdown file from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/markdown`
- **Base URL:** `https://api-server.compdf.com/server`
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
