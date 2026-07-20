# Restore Document with Zoho Writer

Restores a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/restore`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Restore Document](https://www.zoho.com/writer/help/api/v1/restore-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
