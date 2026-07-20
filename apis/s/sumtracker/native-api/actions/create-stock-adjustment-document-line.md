# Create Stock Adjustment Document Line with Sumtracker

Creates a stock adjustment document line in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/:document_id/lines/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Stock Adjustment Document Line](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinecreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Stock adjustment document ID. |
| `product_id` | body | `number` | yes | — |
| `quantity` | body | `number` | yes | — |
