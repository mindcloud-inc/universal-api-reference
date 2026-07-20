# List Purchase Orders with Megaventory

Retrieves purchase order records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/PurchaseOrderGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Purchase Orders](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `mvPurchaseOrderNo` | body | `string` | no | Filter results to a specific purchase order number. |
| `mvPurchaseOrderStatus` | body | `string` | no | Filter results to a specific purchase order status. |
