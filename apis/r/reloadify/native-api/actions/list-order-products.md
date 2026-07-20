# List Order Products with Reloadify

Retrieves products for an order in Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/orders/:order_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Order Products](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrdersOrderIdProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `order_id` | path | `string` | yes | Order identifier. |
