# Magic Color with ComPDFKit PDF Converter

Creates a color-enhanced document from an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/documentAI/magicColor`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [Magic Color](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
