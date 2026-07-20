# Delete Watermark with ComPDFKit PDF Editor

Creates a watermark removal task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/pdf/delWatermark`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [Delete Watermark](https://api.compdf.com/api-reference/watermark-guides)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
