# List Coupons with WooCommerce

Retrieves coupons from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/coupons`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [List Coupons](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-coupons)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to those matching a string. |
| `after` | query | `string` | no | Limit response to resources published after a given ISO8601 date. |
| `before` | query | `string` | no | Limit response to resources published before a given ISO8601 date. |
| `code` | query | `string` | no | Limit result set to resources with a specific code. |
