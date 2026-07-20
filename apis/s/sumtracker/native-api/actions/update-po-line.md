# Update Purchase Order Line with Sumtracker

Updates a purchase order line in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Purchase Order Line](https://developers.sumtracker.com/reference/polineupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cost` | body | `number` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Purchase order line ID. |
| `notes` | body | `string` | no | — |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `product` | body | `number` | no | — |
| `quantity` | body | `number` | no | — |
| `tax_id` | body | `number` | no | — |
