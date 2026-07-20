# List Products with WooCommerce

Retrieves products from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [List Products](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to those matching a string. |
| `after` | query | `string` | no | Limit response to resources published after a given ISO8601 date. |
| `before` | query | `string` | no | Limit response to resources published before a given ISO8601 date. |
| `status` | query | `list<string>` | no | Limit result set to products assigned a specific status. Accepted values: `any`, `draft`, `pending`, `private`, `publish`. |
| `sku` | query | `string` | no | Limit result set to products with a specific SKU. |
