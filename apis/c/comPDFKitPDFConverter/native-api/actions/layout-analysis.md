# Layout Analysis with ComPDFKit PDF Converter

Creates layout analysis output from a document.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/process/documentAI/layoutAnalysis`
- **Base URL:** `https://api-server.compdf.com/server`
- **Official documentation:** [Layout Analysis](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
