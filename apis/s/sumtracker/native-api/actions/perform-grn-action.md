# Perform Goods Receipt Note Action with Sumtracker

Performs an action on a goods receipt note in Sumtracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/perform_action/:id/:action/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [Perform Goods Receipt Note Action](https://developers.sumtracker.com/reference/performactiongrn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | GRN action to perform, such as `mark-received`, `undo-receive`, `mark-final`, or `cancel`. |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | path | `string` | yes | Goods receipt note ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
