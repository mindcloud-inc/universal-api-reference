# Image Distortion Correction with ComPDFKit PDF Editor

Creates an image distortion correction task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/documentAI/dewarp`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [Image Distortion Correction](https://api.compdf.com/api-reference/overview)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
