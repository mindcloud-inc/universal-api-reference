# Upload File For OCR with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Upload File For OCR](https://ocr.space/ocrapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Local image or PDF file to upload for OCR. |
| `language` | body | `string` | no | Three-letter OCR language code. |
| `scale` | body | `boolean` | no | Upscale low-resolution scans before OCR. |
| `detectOrientation` | body | `boolean` | no | Auto-rotate the document before OCR when needed. |
