# Run OCR with PDF-app

Retrieves OCR text from a file in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocr`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Run OCR](https://pdf-app.net/apidocumentation?type=ocr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `versionMode` | body | `string` | no | OCR engine version mode; use 2 for the Textract-based V2 flow. |
| `fileUrls[]` | body | `array<string>` | yes | Document URLs to run through OCR. |
| `v2rawText` | body | `boolean` | no | Whether to extract raw text lines in OCR V2. |
| `v2Layout` | body | `boolean` | no | Whether to include layout blocks and bounding boxes. |
| `v2Forms` | body | `boolean` | no | Whether to extract key-value form pairs. |
| `v2Tables` | body | `boolean` | no | Whether to extract tables from the document. |
| `v2Signatures` | body | `boolean` | no | Whether to detect signatures in the document. |
| `async` | body | `boolean` | no | Whether to run OCR asynchronously. |
| `pdfConvertZoomFactor` | body | `number` | no | Zoom factor used when converting PDFs before OCR. |
| `zoom_factor_img` | body | `number` | no | Scaling factor applied to images before OCR. |
| `regions[]` | body | `array<object>` | no | Optional region definitions for targeted OCR extraction. |
