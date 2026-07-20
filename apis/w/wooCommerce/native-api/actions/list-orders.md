# List Orders with WooCommerce

Retrieves orders from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [List Orders](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to those matching a string. |
| `after` | query | `string` | no | Limit response to resources published after a given ISO8601 date. |
| `before` | query | `string` | no | Limit response to resources published before a given ISO8601 date. |
| `status` | query | `list<string>` | no | Limit result set to orders assigned a specific status. Accepted values: `any`, `cancelled`, `completed`, `failed`, `on-hold`, `pending`, `processing`, `refunded`, `trash`. |
| `customer` | query | `list<number>` | no | Limit result set to orders assigned to a specific customer. |
| `product` | query | `list<number>` | no | Limit result set to orders assigned to a specific product. |
| `order` | query | `string` | no | — |
| `modified_after` | query | `string` | no | — |
| `meta_key` | query | `string` | no | — |
| `meta_value` | query | `string` | no | — |
