# Bulk Update Purchase Orders with Megaventory

Updates purchase orders in Megaventory in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/PurchaseOrdersUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Bulk Update Purchase Orders](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrdersUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrders` | body | `list<object>` | yes | JSON array of purchase order objects. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
