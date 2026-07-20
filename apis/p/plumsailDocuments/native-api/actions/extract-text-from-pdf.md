# Extract Text from PDF with Plumsail Documents

Extracts text from a PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/pdf-to-text`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Extract Text from PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ResultType` | body | `string` | no |
| `Password` | body | `string` | no |
| `StartPage` | body | `number` | no |
| `EndPage` | body | `number` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
