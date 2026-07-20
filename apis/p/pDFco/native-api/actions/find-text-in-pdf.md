# Find Text in PDF with PDF.co

Finds text in a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/find`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Find Text in PDF](https://docs.pdf.co/api-tester/pdf-find/basic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL accessible by PDF.co. |
| `searchstring` | body | `string` | yes | Text to search for in the PDF. |
| `async` | body | `boolean` | no | Set true to run as async job. |
