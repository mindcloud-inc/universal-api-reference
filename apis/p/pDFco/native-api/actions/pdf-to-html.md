# PDF to HTML with PDF.co

Converts a PDF to HTML in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/convert/to/html`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF to HTML](https://docs.pdf.co/api-tester/pdf-to-html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | no | Optional page selection. |
| `async` | body | `boolean` | no | Set true to run as async job. |
