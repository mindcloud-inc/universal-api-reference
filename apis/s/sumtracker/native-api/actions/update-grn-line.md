# Update Goods Receipt Note Line with Sumtracker

Updates a goods receipt note line in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Update Goods Receipt Note Line](https://developers.sumtracker.com/reference/grnlineupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `grn_id` | path | `string` | yes | Goods receipt note ID. |
| `id` | path | `string` | yes | Goods receipt note line ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `poline_id` | body | `number` | no | — |
| `quantity` | body | `number` | no | — |
