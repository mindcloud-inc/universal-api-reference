# Perform Purchase Order Action with Sumtracker

Performs an action on a purchase order in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/perform_action/:id/:action/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Perform Purchase Order Action](https://developers.sumtracker.com/reference/performactionpurchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Action to perform, such as `mark-incoming`, `close`, `cancel`, or `generate-pdf`. |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Purchase order or stock transfer ID. |
