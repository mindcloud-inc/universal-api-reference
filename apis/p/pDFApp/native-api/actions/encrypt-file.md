# Encrypt File with PDF-app

Updates a file with password encryption in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/encryptFileExt`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Encrypt File](https://pdf-app.net/apidocumentation?type=encryptFileExt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | File URL to encrypt or decrypt. |
| `selfEncrypt` | body | `object` | no | Encryption settings including algorithm, key, and IV. Runtime verification confirmed `aes256`/`AES256` as accepted algorithm tokens. |
| `fileName` | body | `string` | no | Desired output file name. |
| `command` | body | `string` | no | Whether to encrypt or decrypt the file. |
