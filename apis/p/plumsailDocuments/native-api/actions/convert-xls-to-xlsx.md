# Convert XLS to XLSX with Plumsail Documents

Converts XLS to XLSX in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/xls-to-xlsx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert XLS to XLSX](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | XLS file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to an XLS file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
