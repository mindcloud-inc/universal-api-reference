# Recognize Layout From URL with OCRSpace

## Endpoint

- **Method:** `POST`
- **Path:** `/parse/image`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Recognize Layout From URL](https://ocr.space/ocrapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the remote image or PDF to parse. |
