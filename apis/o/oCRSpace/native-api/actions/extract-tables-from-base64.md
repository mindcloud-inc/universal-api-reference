# Extract Tables From Base64 with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Extract Tables From Base64](https://ocr.space/receiptscanning)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64Image` | body | `string` | yes | Base64-encoded receipt or table image with its data URI prefix. |
| `language` | body | `string` | no | Three-letter OCR language code. |
