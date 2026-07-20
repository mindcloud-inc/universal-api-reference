# Cancel Batch Job with Mistral AI

Cancels an existing batch job in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/jobs/:job_id/cancel`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Cancel Batch Job](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_cancel_batch_job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The ID of the batch job. |
