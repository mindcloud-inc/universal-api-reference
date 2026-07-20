# List Products with GetResponse

Retrieves products from a GetResponse shop.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shopId/products`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Products](https://apireference.getresponse.com/#operation/getProductList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | Shop identifier |
| `query[name]` | query | `string` | no | Search products by name |
| `query[vendor]` | query | `string` | no | Search products by vendor |
| `query[category]` | query | `string` | no | Search products by category name |
| `query[categoryId]` | query | `string` | no | Search products by category ID |
| `query[externalId]` | query | `string` | no | Search products by external ID |
| `query[variantName]` | query | `string` | no | Search products by product variant name |
| `query[metaFieldNames]` | query | `string` | no | Comma-separated meta field names to search |
| `query[metaFieldValues]` | query | `string` | no | Comma-separated meta field values to search |
| `query[createdOn][from]` | query | `string` | no | Search products created from this date |
| `query[createdOn][to]` | query | `string` | no | Search products created to this date |
| `sort[name]` | query | `string` | no | Sort by name |
| `sort[createdOn]` | query | `string` | no | Sort by date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
