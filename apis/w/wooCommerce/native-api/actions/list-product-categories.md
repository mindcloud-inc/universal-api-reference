# List Product Categories with WooCommerce

Retrieves product categories from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/categories`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [List Product Categories](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-product-categories)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to those matching a string. |
| `slug` | query | `string` | no | Limit result set to resources with a specific slug. |
| `parent` | query | `list<number>` | no | Limit result set to resources assigned to a specific parent. |
| `product` | query | `list<number>` | no | Limit result set to resources assigned to a specific product. |
| `hide_empty` | query | `boolean` | no | Whether to hide resources not assigned to any products. |
