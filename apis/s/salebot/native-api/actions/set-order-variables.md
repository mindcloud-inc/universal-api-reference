# Set Order Variables with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/set_order_vars`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Set Order Variables](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Existing Salebot client ID. |
| `order_id` | body | `number` | yes | Existing Salebot order ID. |
| `variables` | body | `object` | yes | Key-value map of order variables to save. |
