# Convert HTML to PDF with PDF.co

Creates a PDF from HTML in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/from/html`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Convert HTML to PDF](https://docs.pdf.co/api-tester/pdf-from-html/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Source HTML content to convert into PDF. |
| `name` | body | `string` | no | Optional output file name. |
