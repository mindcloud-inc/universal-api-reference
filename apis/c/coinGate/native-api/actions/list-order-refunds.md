# List Order Refunds with CoinGate

Retrieves refunds for a specific CoinGate order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:order_id/refunds`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [List Order Refunds](https://developer.coingate.com/reference/get-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | CoinGate order ID. |
