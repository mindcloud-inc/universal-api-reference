# Create Purchase Order or Stock Transfer with Sumtracker

Creates a purchase order or stock transfer in Sumtracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/version/2025-03/purchases/:document_type/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Create Purchase Order or Stock Transfer](https://developers.sumtracker.com/reference/purchaseordercreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | no | — |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `from_warehouse_id` | body | `number` | no | — |
| `notes` | body | `string` | no | — |
| `reference` | body | `string` | no | — |
| `warehouse_id` | body | `number` | no | — |
