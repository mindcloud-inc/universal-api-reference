# Convert DOCX to PDF with Plumsail Documents

Converts DOCX to PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/docx-to-pdf`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert DOCX to PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | DOCX file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a DOCX file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
