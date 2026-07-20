# Create Stock Adjustment Line with Sumtracker

Creates a stock adjustment line in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/stock/adjustment/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Stock Adjustment Line](https://developers.sumtracker.com/reference/stockadjustmentlinecreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adjustment_type` | body | `string` | no | Stock adjustment type. |
| `product` | body | `number` | no | — |
| `quantity` | body | `number` | yes | — |
| `reason` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
