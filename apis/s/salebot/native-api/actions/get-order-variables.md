# Get Order Variables with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/get_order_vars`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Get Order Variables](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Existing Salebot client ID. |
| `order_id` | body | `number` | yes | Existing Salebot order ID. |
| `variables[]` | body | `array<string>` | no | Variable names to return for the order. |
