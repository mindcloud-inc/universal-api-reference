# List Goods Receipt Notes with Sumtracker

Retrieves goods receipt notes from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/purchases/:document_type/:po_id/grns/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Goods Receipt Notes](https://developers.sumtracker.com/reference/grnlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type` | path | `string` | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `po_id` | path | `string` | yes | Purchase order or stock transfer ID. |
