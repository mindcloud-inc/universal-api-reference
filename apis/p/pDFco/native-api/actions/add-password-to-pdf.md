# Add Password to PDF with PDF.co

Adds a password to a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/security/add`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Add Password to PDF](https://docs.pdf.co/api-tester/pdf-password/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `userPassword` | body | `string` | yes | Password required to open the PDF. |
| `ownerPassword` | body | `string` | no | Owner password for permissions control. |
| `async` | body | `boolean` | no | Set true to run as async job. |
