# Create Batch with Grok

Creates a new batch in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Create Batch](https://docs.x.ai/developers/rest-api-reference/inference/batches#create-a-new-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_name` | body | `string` | no | Optional human-readable batch name. |
| `batch_requests[]` | body | `array<object>` | yes | Requests to include in the new batch. |
