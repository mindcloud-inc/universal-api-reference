# Document Extract with ComPDFKit PDF Converter

Creates document extraction output from an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/idp/documentExtract`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [Document Extract](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
