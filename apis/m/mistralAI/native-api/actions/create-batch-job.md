# Create Batch Job with Mistral AI

Creates a new batch job in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/jobs`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Create Batch Job](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_create_batch_job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `string` | yes | Endpoint path that the batch job should execute. |
| `input_files[]` | body | `array<string>` | no | Uploaded JSONL input files for the batch job. |
| `requests[]` | body | `array<object>` | no | Inline batch request objects. |
| `model` | body | `string` | no | Optional model override for the batch job. |
| `agent_id` | body | `string` | no | Optional deprecated agent ID for the batch job. |
| `metadata` | body | `object` | no | Metadata to associate with the batch job. |
| `timeout_hours` | body | `number` | no | Timeout in hours for the batch job. |
