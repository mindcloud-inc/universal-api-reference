# Upload Table Attachment with Caspio

Uploads a table attachment to Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/tables/{tableName}/attachments/{attachmentFieldName}/{recordPkId}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Upload Table Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UploadFileToAttachmentTableField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `recordPkId` | path | `string` | yes | Record primary key value. |
