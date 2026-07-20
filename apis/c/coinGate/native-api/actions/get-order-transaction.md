# Get Order Transaction with CoinGate

Retrieves a blockchain transaction for a CoinGate order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:order_id/blockchain_transactions/:id`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Get Order Transaction](https://developer.coingate.com/reference/get-order-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | CoinGate order ID. |
| `id` | path | `string` | yes | CoinGate blockchain transaction ID. |
