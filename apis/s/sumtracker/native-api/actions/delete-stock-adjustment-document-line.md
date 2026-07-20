# Delete Stock Adjustment Document Line with Sumtracker

Deletes a stock adjustment document line from Sumtracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/:document_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Delete Stock Adjustment Document Line](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinedelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Stock adjustment document ID. |
| `id` | path | `string` | yes | Stock adjustment document line ID. |
