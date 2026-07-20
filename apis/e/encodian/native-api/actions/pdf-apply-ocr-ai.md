# PDF Apply OCR AI with Encodian

Applies OCR to a PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/AIOcrPdfDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Apply OCR AI](https://support.encodian.com/hc/en-gb/articles/14286080106908)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
