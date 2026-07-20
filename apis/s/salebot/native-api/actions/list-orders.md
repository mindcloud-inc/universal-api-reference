# List Orders with Salebot

## Endpoint

- **Method:** `GET`
- **Path:** `/get_orders`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [List Orders](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `number` | yes | Existing Salebot client ID. |
| `order_status` | query | `number` | yes | 0 for active, 1 for won, 2 for lost orders. |
