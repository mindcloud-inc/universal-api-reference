# List Batch Requests with Grok

Retrieves a list of requests in a Grok batch.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batches/:batch_id/requests`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [List Batch Requests](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-requests-in-a-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier. |
