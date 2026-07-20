# List Products with Goody

Retrieves active products from Goody.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [List Products](https://developer.ongoody.com/api-reference/products/list-all-active-products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `use_custom_catalog` | query | `boolean` | no | Limit to custom catalog only (for approved API partners) |
| `country_code` | query | `string` | no | Filter by a specific shipping country code |
| `custom_catalog_show_inactive` | query | `boolean` | no | Show inactive products in the custom catalog. Only for Commerce API customers with a custom catalog. |
