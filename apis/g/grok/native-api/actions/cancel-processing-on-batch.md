# Cancel Processing on Batch with Grok

Cancels processing on an existing Grok batch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches/:batch_id:cancel`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Cancel Processing on Batch](https://docs.x.ai/developers/rest-api-reference/inference/batches#cancel-processing-on-a-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier. |
