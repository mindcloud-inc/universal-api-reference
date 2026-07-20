# Generate Email with Stripo

Generates an email in Stripo from external source data.

## Endpoint

- **Method:** `POST`
- **Path:** `/email`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Generate Email](https://api.stripo.email/reference/generateemail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSources[]` | body | `array<object>` | yes | Data sources for generation. Send multiple values as a array. |
| `emailId` | body | `number` | no | Existing email ID to override. |
| `emailName` | body | `string` | no | Name for the generated email. |
| `folderId` | body | `number` | no | Folder ID for the generated email. |
| `preheader` | body | `string` | no | Email preheader. |
| `templateId` | body | `number` | yes | Template with the auto-generated area. |
| `title` | body | `string` | no | Email title. |
