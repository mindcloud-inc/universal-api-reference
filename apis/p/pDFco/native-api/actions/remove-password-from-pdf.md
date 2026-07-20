# Remove Password from PDF with PDF.co

Removes a password from a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/security/remove`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Remove Password from PDF](https://docs.pdf.co/api-tester/pdf-password/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `password` | body | `string` | yes | Current password used to open the PDF. |
| `async` | body | `boolean` | no | Set true to run as async job. |
