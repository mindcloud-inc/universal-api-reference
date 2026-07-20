# List Inventory Items with Stockpilot

Retrieves inventory items from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Inventory Items](https://api.stockpilot.dev/redoc#operation/get_inventory_list_inventory_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Number of items per page |
| `created_at` | query | `string` | no | Filter by creation date in YYYY-MM-DD format |
