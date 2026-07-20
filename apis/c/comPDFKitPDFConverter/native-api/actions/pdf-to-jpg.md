# PDF to JPG with ComPDFKit PDF Converter

Creates JPG images from a PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/pdf/jpg`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [PDF to JPG](https://api.compdf.com/api-reference/conversion-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
