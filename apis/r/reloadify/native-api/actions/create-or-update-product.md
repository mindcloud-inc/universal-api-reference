# Create Or Update Product with Reloadify

Creates or updates a product in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Product](https://app.reloadify.com/api-docs/index.html#/products/putV2LanguagesLanguageIdProducts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `product.brand_id` | body | `string` | no | Existing brand ID. |
| `product.name` | body | `string` | no | Product name. |
| `product.id` | body | `string` | yes | Product identifier. |
