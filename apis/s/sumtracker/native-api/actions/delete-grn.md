# Delete Goods Receipt Note with Sumtracker

Deletes a goods receipt note from Sumtracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Delete Goods Receipt Note](https://developers.sumtracker.com/reference/grndelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Goods receipt note ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
