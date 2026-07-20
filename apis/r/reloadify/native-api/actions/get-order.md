# Get Order with Reloadify

Retrieves an order from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/orders/:order_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Order](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrdersOrderId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `order_id` | path | `string` | yes | Order identifier. |
