# Update Sales Order with Unleashed

Updates an existing sales order in Unleashed.

## Endpoint

- **Method:** `PUT`
- **Path:** `/SalesOrders/:orderGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Update Sales Order](https://apidocs.unleashedsoftware.com/SalesOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderGuid` | path | `string` | yes | The Unleashed sales order GUID. |
| `ExchangeRate` | body | `number` | yes | Exchange rate for the sales order. |
| `OrderStatus` | body | `string` | yes | Order status for the sales order. |
| `Tax.TaxCode` | body | `string` | yes | Tax code for the sales order. |
| `Warehouse.WarehouseCode` | body | `string` | yes | Warehouse code for the sales order warehouse. |
| `Tax.TaxRate` | body | `number` | yes | Tax rate inside the sales order tax object. |
| `Comments` | body | `string` | no | Comments for the sales order. |
