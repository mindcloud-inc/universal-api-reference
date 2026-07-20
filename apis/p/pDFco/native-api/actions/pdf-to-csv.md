# PDF to CSV with PDF.co

Converts a PDF to CSV in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/csv`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to CSV](https://docs.pdf.co/api-tester/pdf-to-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | no | Optional page selection. |
| `async` | body | `boolean` | no | Set true to run as async job. |
