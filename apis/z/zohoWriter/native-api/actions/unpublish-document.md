# Unpublish Document with Zoho Writer

Unpublishes a document in Zoho Writer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/documents/:document_id/publish`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Unpublish Document](https://www.zoho.com/writer/help/api/v1/unpublish-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
