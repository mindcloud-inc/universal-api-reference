# Update Inventory Location with Megaventory

Updates an inventory location in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/InventoryLocationUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Inventory Location](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvInventoryLocation` | body | `object` | yes | Inventory location payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
