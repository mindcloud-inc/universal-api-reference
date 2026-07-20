# OCR Remote Document with Nutrient Document Converter

Applies OCR to a remote document in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [OCR Remote Document](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentUrl` | body | `string` | yes | Publicly reachable image or scanned document URL. |
| `language` | body | `string` | no | OCR language code. |
