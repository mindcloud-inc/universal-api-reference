# Document Extraction with ComPDFKit PDF Editor

Creates a document extraction task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/idp/documentExtract`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [Document Extraction](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
