# Get Order Refund with CoinGate

Retrieves a refund for a specific CoinGate order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:order_id/refunds/:id`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Get Order Refund](https://developer.coingate.com/reference/get-order-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | CoinGate order ID. |
| `id` | path | `number` | yes | CoinGate refund ID. |
