# Parse Image URL with OCRSpace

## Endpoint

- **Method:** `GET`
- **Path:** `/parse/imageurl`
- **Base URL:** `https://api.ocr.space`
- **Official documentation:** [Parse Image URL](https://ocr.space/ocrapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | no | URL of the remote image or PDF to parse. |
| `language` | query | `string` | no | Three-letter OCR language code. |
| `isOverlayRequired` | query | `boolean` | no | Return overlay coordinates for detected text. |
