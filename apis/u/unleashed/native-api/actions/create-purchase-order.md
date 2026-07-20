# Create Purchase Order with Unleashed

Creates a new purchase order in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/PurchaseOrders`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Create Purchase Order](https://apidocs.unleashedsoftware.com/Purchases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Supplier` | body | `object` | no | Supplier object for the purchase order. |
| `Supplier.SupplierCode` | body | `string` | yes | Supplier code for the purchase order supplier. |
| `DeliveryDate` | body | `date` | yes | Requested delivery date for the purchase order. |
| `TaxCode` | body | `string` | yes | Tax code for the purchase order. |
| `TaxRate` | body | `number` | yes | Tax rate for the purchase order. |
| `DiscountRate` | body | `number` | no | Overall purchase order discount rate. |
| `OrderStatus` | body | `string` | yes | Order status for the purchase order. |
| `Warehouse` | body | `object` | no | Warehouse object for the purchase order. |
| `Warehouse.WarehouseCode` | body | `string` | yes | Warehouse code for the purchase order warehouse. |
| `PurchaseOrderLines[].LineNumber` | body | `number` | yes | Line number for the purchase order line. |
| `PurchaseOrderLines[].OrderQuantity` | body | `number` | yes | Ordered quantity for the purchase order line. |
| `PurchaseOrderLines[].UnitPrice` | body | `number` | no | Unit price for the purchase order line. |
| `PurchaseOrderLines[].LineTotal` | body | `number` | yes | Line total for the purchase order line. |
| `PurchaseOrderLines[].LineTax` | body | `number` | yes | Line tax for the purchase order line. |
| `PurchaseOrderLines[].Product.ProductCode` | body | `string` | yes | Product code for the purchase order line product. |
| `SubTotal` | body | `number` | yes | Purchase order subtotal. |
| `TaxTotal` | body | `number` | yes | Purchase order tax total. |
| `Total` | body | `number` | yes | Purchase order total. |
