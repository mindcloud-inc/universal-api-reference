# Create Billing Product with CoinGate

Creates a new billing product in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/products`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Billing Product](https://developer.coingate.com/reference/create-billing-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Billing product name. |
| `price` | body | `string` | yes | Billing product price. |
| `currency_id` | body | `number` | yes | CoinGate currency ID. |
