# Update PDF Password with PDF-app

Updates a PDF password in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/passwModPDFExt`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Update PDF Password](https://pdf-app.net/apidocumentation?type=passwModPDFExt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | PDF file URL to protect or unprotect. |
| `passwordProtected` | body | `string` | no | Password to add or use when removing protection. |
| `fileName` | body | `string` | no | Desired output PDF file name. |
| `command` | body | `string` | no | Whether to addPassword or removePassword. |
