# Create Purchase Order Line with Sumtracker

Creates a purchase order line in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/lines/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Purchase Order Line](https://developers.sumtracker.com/reference/polinecreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cost` | body | `number` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `notes` | body | `string` | no | — |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `product` | body | `number` | no | — |
| `quantity` | body | `number` | yes | — |
| `tax_id` | body | `number` | no | — |
