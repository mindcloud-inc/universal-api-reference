# List Stock Items with Booqable

Retrieves stock item records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock_items`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [List Stock Items](https://developers.booqable.com/#stock-items-list-stock_items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `object` | no | Hash of stock item filters using documented field/operator keys. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example product,barcode,location. |
