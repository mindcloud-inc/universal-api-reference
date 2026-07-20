# Bulk Download OCR PDFs with DocuPipe

Creates bulk OCR PDF download URLs in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/download/bulk-ocr-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download OCR PDFs](https://docs.docupipe.ai/reference/bulk_ocr_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to download as OCR PDFs. |
