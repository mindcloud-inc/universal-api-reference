# Get Extraction Results with Natif.ai

Retrieves extraction results for a document from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/[:documentId]/extractions`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get Extraction Results](https://api.natif.ai/docs#/Document%20Capturing/get_extractions_documents__document_id__extractions_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
| `schema_version` | query | `number` | no | Extraction schema version. Pass `-1` for the latest schema. |
