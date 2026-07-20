# List Customers with YouCan

Retrieves a list of customers from YouCan.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.youcan.shop`
- **Official documentation:** [List Customers](https://developer.youcan.shop/store-admin/customers/listing)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | query | `string` | no |
| `limit` | query | `string` | no |
| `orders` | query | `string` | no |
| `page` | query | `string` | no |
| `q` | query | `string` | no |
| `sort_field` | query | `string` | no |
| `sort_order` | query | `string` | no |
