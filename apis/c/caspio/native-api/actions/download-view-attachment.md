# Download View Attachment with Caspio

Downloads a view attachment from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/views/{viewName}/attachments/{attachmentFieldName}/{recordPkId}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Download View Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DownloadFileFromAttachmentViewField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `recordPkId` | path | `string` | yes | Record primary key value. |
