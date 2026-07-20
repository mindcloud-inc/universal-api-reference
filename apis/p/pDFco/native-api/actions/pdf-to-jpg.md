# PDF to JPG with PDF.co

Converts a PDF to JPG in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/jpg`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to JPG](https://docs.pdf.co/api-tester/pdf-to-image/jpg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | no | Optional page selection. |
| `async` | body | `boolean` | no | Set true to run as async job. |
