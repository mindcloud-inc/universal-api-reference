# Add Product To Category with Reloadify

Adds a product to a category in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/products/:product_id/categories/:category_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Add Product To Category](https://app.reloadify.com/api-docs/index.html#/products/putV2LanguagesLanguageIdProductsProductIdCategoriesCategoryId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `product_id` | path | `string` | yes | Product ID. |
| `category_id` | path | `string` | yes | Category ID. |
