# Bulk Update Sales Orders with Megaventory

Updates sales orders in Megaventory in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesOrdersUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Bulk Update Sales Orders](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrdersUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SalesOrders` | body | `list<object>` | yes | JSON array of sales order objects. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
| `AutoInsertBundledProductRows` | body | `boolean` | no | Automatically insert bundled product rows when Megaventory supports it. |
| `AutoInsertBatchNumbersToProductRows` | body | `boolean` | no | Automatically assign batch numbers to product rows when Megaventory supports it. |
