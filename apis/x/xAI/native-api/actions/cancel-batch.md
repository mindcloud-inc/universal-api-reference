# Cancel Batch with xAI

Cancels a batch in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:batch_id:cancel`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Cancel Batch](https://docs.x.ai/developers/rest-api-reference/inference/batches#cancel-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | no | Batch identifier to cancel. |
