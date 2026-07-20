# Add Content to PDF with PDF.co

Adds content to a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/edit/add`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Add Content to PDF](https://docs.pdf.co/api-tester/pdf-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source PDF file. |
| `annotationsString` | body | `string` | no | JSON string with add/edit instructions. |
