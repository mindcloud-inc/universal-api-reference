# Fill DOCX Merge Fields with Plumsail Documents

Fills merge fields in a DOCX document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/generate/from-fillable-docx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Fill DOCX Merge Fields](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Data` | body | `string` | no | JSON object with values to merge into the DOCX file. |
| `File` | body | `file` | no | DOCX document to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a DOCX document. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
