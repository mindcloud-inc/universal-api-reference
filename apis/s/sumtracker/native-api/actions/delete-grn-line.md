# Delete Goods Receipt Note Line with Sumtracker

Deletes a goods receipt note line from Sumtracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Delete Goods Receipt Note Line](https://developers.sumtracker.com/reference/grnlinedelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `grn_id` | path | `string` | yes | Goods receipt note ID. |
| `id` | path | `string` | yes | Goods receipt note line ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
