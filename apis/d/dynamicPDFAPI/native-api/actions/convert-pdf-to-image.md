# Convert PDF To Image with DynamicPDF

Converts a PDF to images in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf-image`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Convert PDF To Image](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdf` | body | `file` | yes | The PDF document to convert to images. |
| `imageFormat` | query | `list` | no | The output image format. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `pageCount` | query | `number` | no | How many pages to rasterize. Zero returns all pages. |
| `startPageNumber` | query | `number` | no | The first page number to rasterize. |
