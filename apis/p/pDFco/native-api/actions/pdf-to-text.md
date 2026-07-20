# PDF to Text with PDF.co

Creates text from a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/text`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to Text](https://docs.pdf.co/api-tester/pdf-to-text/basic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of PDF file to convert. |
| `pages` | body | `string` | no | Optional page range (e.g. 1-3). |
| `password` | body | `string` | no | Password for protected PDFs. |
| `lang` | body | `string` | no | Language hint for OCR parsing. |
| `inline` | body | `boolean` | no | Return text inline when true. |
| `async` | body | `boolean` | no | Process conversion as background job. |
| `name` | body | `string` | no | Optional output filename. |
