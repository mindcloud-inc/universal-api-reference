# Add Batch Requests with xAI

Adds batch requests in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:batch_id/requests`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Add Batch Requests](https://docs.x.ai/developers/rest-api-reference/inference/batches#add-batch-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | no | Batch identifier to add requests to. |
| `batch_requests[]` | body | `array<object>` | no | List of batch requests to add to the batch. |
