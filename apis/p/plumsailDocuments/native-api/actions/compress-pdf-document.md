# Compress PDF Document with Plumsail Documents

Compresses a PDF document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/pdf/compress`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Compress PDF Document](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `LosslessMode` | body | `string` | no |
| `Password` | body | `string` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
