# Add Batch Requests to Batch with Grok

Creates batch requests in a Grok batch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches/:batch_id/requests`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Add Batch Requests to Batch](https://docs.x.ai/developers/rest-api-reference/inference/batches#add-batch-requests-to-a-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier. |
| `batch_requests[]` | body | `array<object>` | yes | Requests to append to the batch. |
