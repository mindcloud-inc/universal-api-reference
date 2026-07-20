# Extract Tables From URL with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Extract Tables From URL](https://ocr.space/receiptscanning)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the receipt or table image to parse. |
| `language` | body | `string` | no | Three-letter OCR language code. |
