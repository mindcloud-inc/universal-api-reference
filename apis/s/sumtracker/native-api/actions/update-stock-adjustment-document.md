# Update Stock Adjustment Document with Sumtracker

Updates a stock adjustment document in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Stock Adjustment Document](https://developers.sumtracker.com/reference/stockadjustmentdocumentupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adjustment_type` | body | `string` | no | Stock adjustment type. |
| `id` | path | `string` | yes | Stock adjustment document ID. |
| `notes` | body | `string` | no | — |
| `reason` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
