# PDF to JSON with PDF.co

Creates JSON data from a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/json2`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to JSON](https://docs.pdf.co/api-tester/pdf-to-json/basic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of PDF file to convert. |
| `pages` | body | `string` | no | Optional page range (e.g. 1-3). |
| `password` | body | `string` | no | Password for protected PDFs. |
| `lang` | body | `string` | no | Language hint for OCR parsing. |
| `inline` | body | `boolean` | no | Return output inline when true. |
| `async` | body | `boolean` | no | Process conversion as background job. |
| `name` | body | `string` | no | Optional output filename. |
