# Get Batch Job with Mistral AI

Retrieves batch job details from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batch/jobs/:job_id`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Get Batch Job](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_get_batch_job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The ID of the batch job. |
| `inline` | query | `boolean` | no | Include inline result content in the response. |
