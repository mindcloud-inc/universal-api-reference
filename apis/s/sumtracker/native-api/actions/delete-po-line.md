# Delete Purchase Order Line with Sumtracker

Deletes a purchase order line from Sumtracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Delete Purchase Order Line](https://developers.sumtracker.com/reference/polinedelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Purchase order line ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
