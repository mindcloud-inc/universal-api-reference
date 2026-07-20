# Mark Stock Adjustment Complete with Sumtracker

Marks a stock adjustment document complete in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/perform_action/:id/mark-complete/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Mark Stock Adjustment Complete](https://developers.sumtracker.com/reference/performactionstockadjustment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Stock adjustment document ID. |
