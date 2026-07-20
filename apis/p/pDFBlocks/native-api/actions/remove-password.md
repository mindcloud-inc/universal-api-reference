# Remove Password with PDF Blocks

Updates a PDF document by removing its password in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/remove_password`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Remove Password](https://www.pdfblocks.com/docs/api/remove-password-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `password` | body | `string` | yes | The password required to open the file. |
