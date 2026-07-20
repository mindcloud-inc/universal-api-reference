# Create HTML Document with Plumsail Documents

Creates an HTML document in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/generate/from-html`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Create HTML Document](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Locale` | body | `string` | no | Locale used to format dates, numbers, and currencies in the output document. |
| `Data` | body | `string` | no | JSON object with values to merge into the HTML template. |
| `Timezone` | body | `string` | no | IANA timezone used for date tokens and date formatting. |
| `File` | body | `file` | no | HTML template file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to an HTML template file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
