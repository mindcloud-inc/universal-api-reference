# Protect PDF Document with Plumsail Documents

Protects a PDF document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/pdf/protect`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Protect PDF Document](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AllowPrinting` | body | `boolean` | yes |
| `AllowModification` | body | `boolean` | yes |
| `AllowExtract` | body | `boolean` | yes |
| `AllowAnnotate` | body | `boolean` | yes |
| `NewOwnerPassword` | body | `string` | no |
| `NewUserPassword` | body | `string` | no |
| `Password` | body | `string` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
