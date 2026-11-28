# List Products with Booqable

Retrieves product records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://{companySlug}.booqable.com/api/4`
- **Official documentation:** [List Products](https://developers.booqable.com/#products-list-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Booqable filters as a JSON object, for example {"archived":{"eq":false}}. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
