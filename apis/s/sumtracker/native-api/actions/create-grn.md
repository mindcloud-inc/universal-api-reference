# Create Goods Receipt Note with Sumtracker

Creates a goods receipt note in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Goods Receipt Note](https://developers.sumtracker.com/reference/grncreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivery_time` | body | `date` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `notes` | body | `string` | no | — |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
| `reference` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
