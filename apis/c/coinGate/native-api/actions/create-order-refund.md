# Create Order Refund with CoinGate

Creates a refund for a specific CoinGate order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:order_id/refunds`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Order Refund](https://developer.coingate.com/reference/create-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | CoinGate order ID. |
| `amount` | body | `number` | yes | Refund amount. |
| `address` | body | `string` | yes | Refund destination address. |
| `currency_id` | body | `number` | yes | CoinGate currency ID. |
| `platform_id` | body | `number` | yes | CoinGate platform ID. |
| `reason` | body | `string` | yes | Refund reason. |
| `email` | body | `string` | yes | Refund contact email. |
| `ledger_account_id` | body | `string` | yes | CoinGate ledger account ID. |
