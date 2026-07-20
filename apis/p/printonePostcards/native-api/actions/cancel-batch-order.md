# Cancel Batch Order with Print.one Postcards

Cancels a batch order in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/batches/:batchId/orders/:orderId/cancel`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Cancel Batch Order](https://api.print.one/docs/v2#operation/Batch/cancelOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | The batch ID. |
| `orderId` | path | `string` | yes | The order ID. |
