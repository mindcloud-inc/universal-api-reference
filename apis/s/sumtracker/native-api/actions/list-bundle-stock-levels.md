# List Bundle Stock Levels with Sumtracker

Retrieves bundle stock levels from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-11/stock/levels/bundles/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Cursor
- **Official documentation:** [List Bundle Stock Levels](https://developers.sumtracker.com/reference/stocklevelbundlelist-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor returned by the previous 2025-11 bundle stock-level response. |
| `product` | query | `number` | no | Bundle product ID. |
| `warehouse` | query | `number` | no | Warehouse ID. |
