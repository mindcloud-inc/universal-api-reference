# Create Batch with Cerebras AI

Creates a batch in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Create Batch](https://inference-docs.cerebras.ai/api-reference/batch/create-batch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input_file_id` | body | `string` | yes |
| `endpoint` | body | `string` | yes |
| `completion_window` | body | `string` | yes |
