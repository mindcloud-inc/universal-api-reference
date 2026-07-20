# Delete View Attachment with Caspio

Deletes a view attachment from Caspio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/views/{viewName}/attachments/{attachmentFieldName}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Delete View Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DeleteFileFromAttachmentViewFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
