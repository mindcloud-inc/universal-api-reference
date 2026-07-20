# Cancel Purchase Order with Megaventory

Cancels a purchase order in Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/PurchaseOrderCancel`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Cancel Purchase Order](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderCancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvPurchaseOrderNoToCancel` | body | `string` | yes | Purchase order number Megaventory should cancel. |
| `mvPurchaseOrderTypeId` | body | `number` | yes | Purchase order type ID Megaventory needs for cancellation. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
