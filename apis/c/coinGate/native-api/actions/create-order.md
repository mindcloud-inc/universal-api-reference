# Create Order with CoinGate

Creates a new order in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Order](https://developer.coingate.com/reference/create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `price_amount` | body | `number` | yes | Order price amount. |
| `price_currency` | body | `string` | yes | Order price currency. |
| `title` | body | `string` | yes | Order title. |
| `description` | body | `string` | yes | Order description. |
