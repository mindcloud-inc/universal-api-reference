# List Customers with WooCommerce

Retrieves customers from WooCommerce.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [List Customers](https://woocommerce.github.io/woocommerce-rest-api-docs/#list-all-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Limit results to those matching a string. |
| `email` | query | `string` | no | Limit result set to resources with a specific email. |
| `role` | query | `string` | no | Limit result set to resources with a specific role. |
