# List Batch Orders with Print.one Postcards

Retrieves batch orders from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/batches/:batchId/orders`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [List Batch Orders](https://api.print.one/docs/v2#operation/Batch/getOrderList)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID whose orders to list |
