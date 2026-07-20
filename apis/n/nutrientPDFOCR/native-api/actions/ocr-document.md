# OCR Document with Nutrient - PDF OCR

Retrieves a searchable PDF from Nutrient using OCR.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/ocr`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [OCR Document](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image or scanned document to run OCR on. |
| `data.language` | body | `string` | yes | OCR language to use. Nutrient's example uses english. |
