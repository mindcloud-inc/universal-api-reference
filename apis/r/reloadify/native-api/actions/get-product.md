# Get Product with Reloadify

Retrieves a product from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/products/:product_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Product](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `product_id` | path | `string` | yes | Product ID. |
