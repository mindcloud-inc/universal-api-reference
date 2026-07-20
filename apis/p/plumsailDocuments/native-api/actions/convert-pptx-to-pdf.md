# Convert PPTX to PDF with Plumsail Documents

Converts PPTX to PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/pptx-to-pdf`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert PPTX to PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | PPTX file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a PPTX file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
