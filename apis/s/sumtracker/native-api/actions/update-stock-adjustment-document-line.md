# Update Stock Adjustment Document Line with Sumtracker

Updates a stock adjustment document line in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/:document_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Stock Adjustment Document Line](https://developers.sumtracker.com/reference/stockadjustmentdocumentlineupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Stock adjustment document ID. |
| `id` | path | `string` | yes | Stock adjustment document line ID. |
| `product` | body | `number` | no | — |
| `quantity` | body | `number` | no | — |
