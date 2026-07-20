# Delete Document with Natif.ai

Deletes an existing document from Natif.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/[:documentId]`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Delete Document](https://api.natif.ai/docs#/Document%20Capturing/delete_document_documents__document_id__delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document to delete. |
