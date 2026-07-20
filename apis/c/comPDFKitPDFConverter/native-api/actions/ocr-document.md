# OCR Document with ComPDFKit PDF Converter

Creates OCR output from a document file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/documentAI/ocr`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [OCR Document](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
