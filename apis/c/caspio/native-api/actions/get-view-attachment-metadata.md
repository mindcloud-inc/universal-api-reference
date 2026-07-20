# Get View Attachment Metadata with Caspio

Retrieves view attachment metadata from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/views/{viewName}/attachments/{attachmentFieldName}/fileInfo`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Get View Attachment Metadata](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/GetFileMetadataFromAttachmentViewFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
