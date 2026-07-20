# Rename Table Attachment with Caspio

Updates table attachment metadata in Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Rename Table Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UpdateFileMetadataInAttachmentTableFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
| `response` | query | `string` | no | Optional response type. |
| `FileName` | body | `string` | yes | New file name. |
