# List Purchase Orders with SOS Inventory

Retrieves purchase orders from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/purchaseorder`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Purchase Orders](https://developer.sosinventory.com/apidoc/PurchaseOrder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by open or closed purchase orders. |
| `query` | query | `string` | no | Match order number, comment, vendor name, or customer name. |
| `archived` | query | `string` | no | Use yes for archived only or no for active only. |
| `from` | query | `string` | no | Beginning transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `to` | query | `string` | no | Ending transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `createdsince` | query | `string` | no | Return transactions created since this timestamp. |
| `updatedsince` | query | `string` | no | Return transactions updated since this timestamp. |
