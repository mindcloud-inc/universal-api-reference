# Update Goods Receipt Note with Sumtracker

Updates a goods receipt note in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Goods Receipt Note](https://developers.sumtracker.com/reference/grnupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivery_time` | body | `date` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Goods receipt note ID. |
| `notes` | body | `string` | no | — |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `reference` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
