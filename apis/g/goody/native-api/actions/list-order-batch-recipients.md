# List Order Batch Recipients with Goody

Retrieves recipients for an order batch in Goody.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/order_batches/:id/recipients`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [List Order Batch Recipients](https://developer.ongoody.com/api-reference/order-batches/retrieve-recipients-for-an-order-batch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Order batch ID |
