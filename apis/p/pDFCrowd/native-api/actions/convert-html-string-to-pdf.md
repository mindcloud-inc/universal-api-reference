# Convert HTML String to PDF with PDFCrowd

Creates a PDF from an HTML string in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert HTML String to PDF](https://pdfcrowd.com/api/html-to-pdf-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Raw HTML markup to convert into a PDF document. |
