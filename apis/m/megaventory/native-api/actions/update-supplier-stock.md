# Update Supplier Stock with Megaventory

Updates supplier stock in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SupplierStockUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Supplier Stock](https://api.megaventory.com/v2017a/json/metadata?op=SupplierStockUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvSupplierStockUpdate` | body | `object` | yes | Supplier stock payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
