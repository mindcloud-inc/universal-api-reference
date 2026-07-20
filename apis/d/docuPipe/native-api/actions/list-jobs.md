# List Jobs with DocuPipe

Retrieves jobs from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Jobs](https://docs.docupipe.ai/reference/list_jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

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
