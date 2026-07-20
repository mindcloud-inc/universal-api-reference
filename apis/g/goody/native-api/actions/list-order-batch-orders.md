# List Order Batch Orders with Goody

Retrieves orders for an order batch in Goody.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/order_batches/:id/orders`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [List Order Batch Orders](https://developer.ongoody.com/api-reference/order-batches/retrieve-orders-for-an-order-batch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Order batch ID |
