# Get Processed Page Images with Natif.ai

Retrieves processed page images for a document from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/[:documentId]/processed`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get Processed Page Images](https://api.natif.ai/docs#/Document%20Capturing/get_processed_pages_documents__document_id__processed_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
| `scaled` | query | `boolean` | no | Return page images scaled down by factor 0.4. |
