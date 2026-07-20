# Split PDF with PDF.co

Creates split PDF files in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/split`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Split PDF](https://docs.pdf.co/api-reference/pdf-split/by-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of PDF file to split. |
| `pages` | body | `string` | no | Pages or page ranges to extract. |
| `name` | body | `string` | no | Optional output filename. |
| `async` | body | `boolean` | no | Process split as background job. |
