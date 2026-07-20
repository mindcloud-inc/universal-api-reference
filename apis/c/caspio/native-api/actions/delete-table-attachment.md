# Delete Table Attachment with Caspio

Deletes a table attachment from Caspio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/tables/{tableName}/attachments/{attachmentFieldName}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Delete Table Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/DeleteFileFromAttachmentTableFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
