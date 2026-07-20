# Create Stock Adjustment Document with Sumtracker

Creates a stock adjustment document in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Stock Adjustment Document](https://developers.sumtracker.com/reference/stockadjustmentdocumentcreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adjustment_type` | body | `string` | no | Stock adjustment type. |
| `notes` | body | `string` | no | — |
| `reason` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
