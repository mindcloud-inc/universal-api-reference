# List Order Transactions with CoinGate

Retrieves blockchain transactions for a specific CoinGate order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:order_id/blockchain_transactions`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [List Order Transactions](https://developer.coingate.com/reference/get-order-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | CoinGate order ID. |
