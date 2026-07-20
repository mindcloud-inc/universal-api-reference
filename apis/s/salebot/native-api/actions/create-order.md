# Create Order with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/create_order`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Create Order](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Existing Salebot client ID. |
| `name` | body | `string` | no | Order name. |
| `description` | body | `string` | no | Order description. |
| `budget` | body | `number` | no | Order budget or amount. |
| `state_id` | body | `number` | no | Optional target pipeline state ID. |
