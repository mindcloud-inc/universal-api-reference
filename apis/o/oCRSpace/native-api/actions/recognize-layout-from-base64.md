# Recognize Layout From Base64 with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Recognize Layout From Base64](https://ocr.space/ocrapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64Image` | body | `string` | yes | Base64-encoded image or PDF input with its data URI prefix. |
