# Get Shopping Cart with Reloadify

Retrieves a shopping cart from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/shopping_carts/:shopping_cart_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Shopping Cart](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCartsShoppingCartId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `shopping_cart_id` | path | `string` | yes | Shopping cart identifier. |
