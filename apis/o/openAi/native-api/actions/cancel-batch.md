# Cancel Batch with Open AI

Cancels a batch in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/batches/:batch_id/cancel`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Cancel Batch](https://developers.openai.com/api/reference/resources/batches/methods/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | The ID of the batch to cancel. |
