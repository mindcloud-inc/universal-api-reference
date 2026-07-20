# PDF to Editable PDF with ComPDFKit PDF Editor

Creates an editable PDF conversion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/editable`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [PDF to Editable PDF](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
