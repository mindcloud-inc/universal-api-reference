# Add Password with PDF Blocks

Updates a PDF document with a password in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/add_password`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Add Password](https://www.pdfblocks.com/docs/api/add-password-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `password` | body | `string` | yes | The password required to open the file. |
| `encryption_algorithm` | body | `string` | no | The algorithm used to encrypt the PDF document. |
