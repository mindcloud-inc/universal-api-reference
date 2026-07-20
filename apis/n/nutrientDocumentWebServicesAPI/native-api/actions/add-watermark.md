# Add Watermark with Nutrient Document Web Services

Updates a document with watermarks in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/watermark`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Watermark](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-watermark)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | PDF file to watermark. |
| `data` | body | `object` | no | Watermark configuration payload. |
