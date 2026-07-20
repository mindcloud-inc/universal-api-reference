# PDF to DOCX with ComPDFKit PDF Converter

Creates a DOCX file from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/docx`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF to DOCX](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file<file>` | yes |
