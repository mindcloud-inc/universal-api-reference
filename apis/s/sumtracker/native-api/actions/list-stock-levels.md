# List Stock Levels with Sumtracker

Retrieves stock levels from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-11/stock/levels/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Cursor
- **Official documentation:** [List Stock Levels](https://developers.sumtracker.com/reference/stocklevellist-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor returned by the previous 2025-11 stock-level response. |
| `product` | query | `number` | no | Product ID. Either product or warehouse is required by Sumtracker. |
| `warehouse` | query | `number` | no | Warehouse ID. Either warehouse or product is required by Sumtracker. |
