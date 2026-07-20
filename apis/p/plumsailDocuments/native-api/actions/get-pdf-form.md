# Get PDF Form with Plumsail Documents

Retrieves form fields from a PDF in Plumsail Documents.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/pdf/get-form`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Get PDF Form](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Password` | body | `string` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
