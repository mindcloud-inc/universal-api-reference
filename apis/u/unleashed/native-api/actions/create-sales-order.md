# Create Sales Order with Unleashed

Creates a new sales order in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/SalesOrders`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Create Sales Order](https://apidocs.unleashedsoftware.com/SalesOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer.CustomerCode` | body | `string` | yes | Customer code for the sales order customer. |
| `Warehouse.WarehouseCode` | body | `string` | yes | Warehouse code for the sales order warehouse. |
| `ExchangeRate` | body | `number` | yes | Exchange rate for the sales order. |
| `OrderStatus` | body | `string` | yes | Order status for the sales order. |
| `Tax.TaxCode` | body | `string` | yes | Tax code for the sales order. |
| `Tax.TaxRate` | body | `number` | yes | Tax rate inside the sales order tax object. |
| `TaxRate` | body | `number` | yes | Tax rate for the sales order. |
| `SubTotal` | body | `number` | yes | Sales order subtotal. |
| `TaxTotal` | body | `number` | yes | Sales order tax total. |
| `Total` | body | `number` | yes | Sales order total. |
| `SalesOrderLines[].LineNumber` | body | `number` | yes | Line number for the sales order line. |
| `SalesOrderLines[].Product.ProductCode` | body | `string` | yes | Product code for the sales order line product. |
| `SalesOrderLines[].OrderQuantity` | body | `number` | yes | Ordered quantity for the sales order line. |
| `SalesOrderLines[].UnitPrice` | body | `number` | yes | Unit price for the sales order line. |
| `SalesOrderLines[].LineTotal` | body | `number` | yes | Line total for the sales order line. |
| `SalesOrderLines[].LineTax` | body | `number` | yes | Line tax for the sales order line. |
