# Create DOCX Document with Plumsail Documents

Creates a DOCX document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/generate/from-docx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Create DOCX Document](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Locale` | body | `string` | no | Locale used to format dates, numbers, and currencies in the output document. |
| `Data` | body | `string` | no | JSON object with values to merge into the DOCX template. |
| `OutputType` | body | `string` | no | Optional output format for the generated document. |
| `Timezone` | body | `string` | no | IANA timezone used for date tokens and date formatting. |
| `Engine` | body | `string` | no | Template engine to use for DOCX processing. |
| `File` | body | `file` | no | DOCX template file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a DOCX template file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
