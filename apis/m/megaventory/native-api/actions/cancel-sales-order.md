# Cancel Sales Order with Megaventory

Cancels a sales order in Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesOrderCancel`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Cancel Sales Order](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderCancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvSalesOrderNoToCancel` | body | `string` | yes | Sales order number Megaventory should cancel. |
| `mvSalesOrderTypeId` | body | `number` | yes | Sales order type ID Megaventory needs for cancellation. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
