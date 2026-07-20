# Get Table Attachment Metadata with Caspio

Retrieves table attachment metadata from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Get Table Attachment Metadata](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/GetFileMetadataFromAttachmentTableFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
