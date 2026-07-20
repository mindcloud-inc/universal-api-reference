# PDF to XLSX with PDF.co

Converts a PDF to XLSX in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/xlsx`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to XLSX](https://docs.pdf.co/api-tester/pdf-to-excel/xlsx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | no | Optional page selection. |
| `async` | body | `boolean` | no | Set true to run as async job. |
