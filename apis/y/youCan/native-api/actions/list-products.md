# List Products with YouCan

Retrieves a list of products from YouCan.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.youcan.shop`
- **Official documentation:** [List Products](https://developer.youcan.shop/store-admin/products/listing)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventory` | query | `string` | no |
| `limit` | query | `string` | no |
| `page` | query | `string` | no |
| `q` | query | `string` | no |
| `sort_field` | query | `string` | no |
| `sort_order` | query | `string` | no |
| `trashed` | query | `string` | no |
