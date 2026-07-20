# List Batch Jobs with Mistral AI

Retrieves batch jobs from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batch/jobs`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [List Batch Jobs](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_get_batch_jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | query | `string` | no | Optional model filter. |
| `agent_id` | query | `string` | no | Optional agent filter. |
| `metadata` | query | `object` | no | Optional metadata filter object. |
| `created_after` | query | `string` | no | Only return jobs created after this timestamp. |
| `created_by_me` | query | `boolean` | no | Only return jobs created by the current user. |
| `status[]` | query | `array<string>` | no | Optional batch job status filter list. |
| `order_by` | query | `string` | no | Sort order for batch jobs. |
