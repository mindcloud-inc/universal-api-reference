# List Coupons with YouCan

Retrieves a list of coupons from YouCan.

## Endpoint

- **Method:** `GET`
- **Path:** `/coupons`
- **Base URL:** `https://api.youcan.shop`
- **Official documentation:** [List Coupons](https://developer.youcan.shop/store-admin/coupons/listing)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `string` | no |
| `page` | query | `string` | no |
| `q` | query | `string` | no |
| `sort_field` | query | `string` | no |
| `sort_order` | query | `string` | no |
