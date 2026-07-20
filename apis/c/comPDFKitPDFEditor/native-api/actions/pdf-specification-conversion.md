# PDF Specification Conversion with ComPDFKit PDF Editor

Creates a PDF specification conversion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/convertType`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF Specification Conversion](https://api.compdf.com/api-reference/pdf-convertType)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
