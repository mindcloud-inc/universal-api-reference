# Parse URL Securely with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Parse URL Securely](https://ocr.space/ocrapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the remote image or PDF to parse. |
| `language` | body | `string` | no | Three-letter OCR language code. |
| `scale` | body | `boolean` | no | Upscale low-resolution scans before OCR. |
| `detectOrientation` | body | `boolean` | no | Auto-rotate the document before OCR when needed. |
