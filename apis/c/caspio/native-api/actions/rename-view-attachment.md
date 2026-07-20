# Rename View Attachment with Caspio

Updates view attachment metadata in Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/views/{viewName}/attachments/{attachmentFieldName}/fileInfo`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Rename View Attachment](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UpdateFileMetadataInAttachmentViewFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `attachmentFieldName` | path | `string` | yes | Attachment field name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the row holding the file. |
| `response` | query | `string` | no | Optional response type. |
| `FileName` | body | `string` | yes | New file name. |
