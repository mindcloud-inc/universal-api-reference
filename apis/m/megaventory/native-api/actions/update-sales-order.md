# Update Sales Order with Megaventory

Updates a sales order in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesOrderUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Sales Order](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvSalesOrder` | body | `object` | yes | Sales order payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
| `AutoInsertBundledProductRows` | body | `boolean` | no | Automatically insert bundled product rows when Megaventory supports it. |
| `AutoInsertBatchNumbersToProductRows` | body | `boolean` | no | Automatically assign batch numbers to product rows when Megaventory supports it. |
