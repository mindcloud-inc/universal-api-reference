# Trash Document with Zoho Writer

Moves a document to trash in Zoho Writer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/documents/:document_id/trash`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Trash Document](https://www.zoho.com/writer/help/api/v1/trash-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
