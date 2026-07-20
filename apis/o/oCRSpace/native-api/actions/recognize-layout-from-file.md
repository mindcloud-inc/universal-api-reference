# Recognize Layout From File with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Recognize Layout From File](https://ocr.space/tablerecognition)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file to upload for OCR Engine 3 layout recognition. |
