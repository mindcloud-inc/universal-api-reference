# PDF to HTML with ComPDFKit PDF Converter

Creates an HTML file from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/html`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF to HTML](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
