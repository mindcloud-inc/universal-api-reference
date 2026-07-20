# List Sales Orders with Megaventory

Retrieves sales order records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SalesOrderGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Sales Orders](https://api.megaventory.com/v2017a/json/metadata?op=SalesOrderGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `mvSalesOrderNo` | body | `string` | no | Filter results to a specific sales order number. |
| `mvSalesOrderStatus` | body | `string` | no | Filter results to a specific sales order status. |
