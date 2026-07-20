# Get Document with Natif.ai

Retrieves a document and its processing status from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/[:documentId]`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get Document](https://api.natif.ai/docs#/Document%20Capturing/get_document_documents__document_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
| `get_process_instance` | query | `boolean` | no | Return detailed processing information for workflow-processed documents. |
