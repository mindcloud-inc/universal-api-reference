# Bulk Download OCR PDFs with DocuPanda - Document Understanding

Creates a bulk OCR PDF download URL in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/download/bulk-ocr-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download OCR PDFs](https://docs.docupipe.ai/reference/bulk_ocr_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to download as OCR PDFs. |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to download as OCR PDFs. |
