# List Warehouse Items with Stockpilot

Retrieves inventory items from a Stockpilot warehouse.

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouses/:unique_id/items`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Warehouse Items](https://api.stockpilot.dev/redoc#operation/get_warehouses_items_warehouses__unique_id__items_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique_id` | path | `string` | yes | Warehouse unique ID |
| `page` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Number of items per page |
| `sku` | query | `string` | no | Filter by SKU |
| `barcode` | query | `string` | no | Filter by barcode |
