# Get Order State with Salebot

## Endpoint

- **Method:** `GET`
- **Path:** `/get_order_state`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Get Order State](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `number` | yes | Existing Salebot client ID. |
| `order_id` | query | `number` | no | Existing Salebot order ID. |
