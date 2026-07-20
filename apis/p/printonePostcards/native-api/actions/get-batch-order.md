# Get Batch Order with Print.one Postcards

Retrieves a batch order from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/batches/:batchId/orders/:orderId`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Batch Order](https://api.print.one/docs/v2#operation/Batch/getBatchOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID to inspect |
| `orderId` | path | `string` | yes | Order ID to inspect |
