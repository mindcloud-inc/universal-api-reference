# Update Purchase Order with Megaventory

Updates a purchase order in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/PurchaseOrderUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Purchase Order](https://api.megaventory.com/v2017a/json/metadata?op=PurchaseOrderUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvPurchaseOrder` | body | `object` | yes | Purchase order payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
