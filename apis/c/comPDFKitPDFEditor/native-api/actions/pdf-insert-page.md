# PDF Insert Page with ComPDFKit PDF Editor

Creates a PDF page insertion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/insert`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF Insert Page](https://api.compdf.com/api-reference/insert)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
