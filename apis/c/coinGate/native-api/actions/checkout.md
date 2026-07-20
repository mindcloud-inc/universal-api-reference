# Checkout with CoinGate

Creates a checkout session for an existing CoinGate order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:id/checkout`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Checkout](https://developer.coingate.com/reference/checkout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | CoinGate order ID. |
| `pay_currency` | body | `string` | yes | Currency to pay with. |
| `platform_id` | body | `number` | yes | CoinGate platform ID. |
