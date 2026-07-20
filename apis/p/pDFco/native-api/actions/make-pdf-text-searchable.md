# Make PDF Text Searchable with PDF.co

Makes a PDF text searchable in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/makesearchable`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Make PDF Text Searchable](https://docs.pdf.co/api-tester/pdf-change-text-searchable/searchable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `language` | body | `string` | no | OCR language code (e.g. eng). |
| `async` | body | `boolean` | no | Set true to run as async job. |
