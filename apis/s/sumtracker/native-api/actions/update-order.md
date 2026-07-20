# Update Purchase Order or Stock Transfer with Sumtracker

Updates a purchase order or stock transfer in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Purchase Order or Stock Transfer](https://developers.sumtracker.com/reference/purchaseorderupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `from_warehouse_id` | body | `number` | no | — |
| `id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `notes` | body | `string` | no | — |
| `reference` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
