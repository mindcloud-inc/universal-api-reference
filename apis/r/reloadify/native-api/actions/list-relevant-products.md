# List Relevant Products with Reloadify

Retrieves relevant products from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/products/:product_id/relevant_products`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Relevant Products](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductIdRelevantProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `product_id` | path | `string` | yes | Product ID. |
