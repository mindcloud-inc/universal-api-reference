# Convert XLSX to PDF with Plumsail Documents

Converts XLSX to PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/xlsx-to-pdf`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert XLSX to PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | XLSX file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to an XLSX file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
