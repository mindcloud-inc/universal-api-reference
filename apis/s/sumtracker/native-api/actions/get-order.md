# Get Purchase Order or Stock Transfer with Sumtracker

Retrieves a purchase order or stock transfer from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/purchases/:document_type/:id/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Get Purchase Order or Stock Transfer](https://developers.sumtracker.com/reference/purchaseorderget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Purchase order or stock transfer ID. |
