# PDF to Editable PDF with ComPDFKit PDF Converter

Creates an editable PDF from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/editable`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF to Editable PDF](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
