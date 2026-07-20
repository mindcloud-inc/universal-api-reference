# Cancel Batch with Voyage

Cancels an in-progress batch in Voyage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches/:batchId/cancel`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Cancel Batch](https://docs.voyageai.com/reference/cancel-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | ID of the batch to cancel. |
