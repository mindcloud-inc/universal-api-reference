# List Goods Receipt Note Lines with Sumtracker

Retrieves goods receipt note lines from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Goods Receipt Note Lines](https://developers.sumtracker.com/reference/grnlinelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `grn_id` | path | `string` | yes | Goods receipt note ID. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
