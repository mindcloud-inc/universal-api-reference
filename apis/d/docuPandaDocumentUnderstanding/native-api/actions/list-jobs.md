# List Jobs with DocuPanda - Document Understanding

Retrieves jobs from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Jobs](https://docs.docupipe.ai/reference/list_jobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `string` | no |
| `end_date` | query | `string` | no |
| `status` | query | `string` | no |
| `job_type` | query | `string` | no |
| `schema_id` | query | `string` | no |
| `document_id` | query | `string` | no |
| `new_document_id` | query | `string` | no |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
