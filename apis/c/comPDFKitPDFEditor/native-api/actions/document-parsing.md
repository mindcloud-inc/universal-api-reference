# Document Parsing with ComPDFKit PDF Editor

Creates a document parsing task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/idp/documentParsing`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [Document Parsing](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
