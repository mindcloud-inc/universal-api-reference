# Upload View Attachment with Caspio

Uploads a view attachment to Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/views/{viewName}/attachments/{attachmentFieldName}/{recordPkId}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Upload View Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UploadFileToAttachmentViewField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `recordPkId` | path | `string` | yes | Record primary key value. |
