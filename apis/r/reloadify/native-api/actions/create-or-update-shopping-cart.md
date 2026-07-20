# Create Or Update Shopping Cart with Reloadify

Creates or updates a shopping cart in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/shopping_carts`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Shopping Cart](https://app.reloadify.com/api-docs/index.html#/shopping_carts/putV2LanguagesLanguageIdShoppingCarts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `shopping_cart.id` | body | `string` | yes | Shopping cart identifier. |
| `shopping_cart.profile_id` | body | `string` | yes | Existing Reloadify profile ID. |
