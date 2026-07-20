# List Cart Products with Reloadify

Retrieves products for a shopping cart in Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/shopping_carts/:shopping_cart_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Cart Products](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCartsShoppingCartIdProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `shopping_cart_id` | path | `string` | yes | Shopping cart identifier. |
