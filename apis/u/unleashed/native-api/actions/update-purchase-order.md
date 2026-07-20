# Update Purchase Order with Unleashed

Updates an existing purchase order in Unleashed.

## Endpoint

- **Method:** `PUT`
- **Path:** `/PurchaseOrders/:orderGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Update Purchase Order](https://apidocs.unleashedsoftware.com/Purchases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderGuid` | path | `string` | yes | The Unleashed purchase order GUID. |
| `Supplier.SupplierCode` | body | `string` | yes | Supplier code for the purchase order supplier. |
| `OrderStatus` | body | `string` | yes | Order status for the purchase order. |
| `Comments` | body | `string` | no | Comments for the purchase order. |
