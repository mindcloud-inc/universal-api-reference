# Convert DOC to DOCX with Plumsail Documents

Converts DOC to DOCX in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/doc-to-docx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert DOC to DOCX](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | DOC file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a DOC file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
