# Create PPTX Document with Plumsail Documents

Creates a PPTX document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/generate/from-pptx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Create PPTX Document](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Locale` | body | `string` | no | Locale used to format dates, numbers, and currencies in the output document. |
| `Data` | body | `string` | no | JSON object with values to merge into the PPTX template. |
| `OutputType` | body | `string` | no | Optional output format for the generated document. |
| `Timezone` | body | `string` | no | IANA timezone used for date tokens and date formatting. |
| `File` | body | `file` | no | PPTX template file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a PPTX template file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
