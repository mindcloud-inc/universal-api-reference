# Parse Image URL With Overlay with OCRSpace

## Endpoint

- **Method:** `GET`
- **Path:** `/parse/imageurl`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Parse Image URL With Overlay](https://ocr.space/ocrapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the remote image or PDF to parse. |
| `language` | query | `string` | no | Three-letter OCR language code. |
