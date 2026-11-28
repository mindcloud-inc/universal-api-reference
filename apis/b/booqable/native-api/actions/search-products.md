# Search Products with Booqable

Finds products in Booqable by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/search`
- **Base URL:** `https://{companySlug}.booqable.com/api/4`
- **Official documentation:** [Search Products](https://developers.booqable.com/#products-search-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Booqable query filters as a JSON object, for example {"archived":{"eq":false}}. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
