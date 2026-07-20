# Find Uploaded Documents with Natif.ai

Finds uploaded documents in Natif.ai by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Find Uploaded Documents](https://api.natif.ai/docs#/Document%20Capturing/get_documents_documents_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of documents to return. |
| `date_from` | query | `date` | no | Filter documents uploaded on or after this ISO 8601 datetime. |
| `date_to` | query | `date` | no | Filter documents uploaded on or before this ISO 8601 datetime. |
| `status` | query | `list` | no | Processing status filter. Accepted values: `All`, `Failed`, `Pending`, `Success`. |
| `postprocessing_status` | query | `list` | no | Postprocessing status filter. Accepted values: `All`, `Auto`, `Manual`, `Pending`, `Rejected`, `Reviewed`, `To Review`, `Warning`. |
| `process_definition_key` | query | `string` | no | Filter documents processed with a specific workflow. |
| `get_process_instance` | query | `boolean` | no | Return detailed processing information for workflow-processed documents. |
