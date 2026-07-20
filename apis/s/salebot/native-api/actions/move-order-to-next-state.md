# Move Order to Next State with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/move_order_to_next_state`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Move Order to Next State](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Existing Salebot client ID. |
| `order_id` | body | `number` | yes | Existing Salebot order ID. |
