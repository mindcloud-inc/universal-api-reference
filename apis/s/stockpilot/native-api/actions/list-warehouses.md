# List Warehouses with Stockpilot

Retrieves warehouses from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouses/get`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Warehouses](https://api.stockpilot.dev/redoc#operation/get_warehouses_list_warehouses_get_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Number of items per page |
