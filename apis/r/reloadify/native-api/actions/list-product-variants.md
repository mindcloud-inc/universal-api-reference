# List Product Variants with Reloadify

Retrieves product variants from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/products/:product_id/variants`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Product Variants](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductIdVariants)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `product_id` | path | `string` | yes | Product ID. |
