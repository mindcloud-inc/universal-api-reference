# Compress PDF with PDF.co

Compresses a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/../v2/pdf/compress`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Compress PDF](https://docs.pdf.co/api-tester/pdf-compress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL accessible by PDF.co. |
| `async` | body | `boolean` | no | Set true to run as async job. |
| `name` | body | `string` | no | Optional output filename. |
