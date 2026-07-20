# List Products with Booqable

Retrieves product records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [List Products](https://developers.booqable.com/#products-list-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `object` | no | Hash of product filters using documented field/operator keys. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
