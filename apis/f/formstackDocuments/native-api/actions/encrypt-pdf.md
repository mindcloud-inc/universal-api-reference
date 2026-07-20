# Encrypt PDF with Formstack Documents

Encrypts a PDF file in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/encrypt_pdf`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Encrypt PDF](https://www.webmerge.me/developers/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file[contents]` | body | `string` | no | Base64-encoded PDF contents |
| `file[name]` | body | `string` | yes | Name of the PDF file to encrypt |
| `file[url]` | body | `string` | no | Remote URL for the PDF file to encrypt |
| `password` | body | `string` | no | Owner password used to edit permissions |
| `user_password` | body | `string` | no | Password required to open the PDF |
