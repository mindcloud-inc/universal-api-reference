# Create Shipment Small Batch with Rithum DSCO

## Endpoint

- **Method:** `POST`
- **Path:** `order/shipment/batch/small`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [Create Shipment Small Batch](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/createShipmentSmallBatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dscoOrderId` | body | `string` | no | DSCO order ID. Provide this or poNumber or supplierOrderNumber to identify the order. |
| `poNumber` | body | `string` | no | Purchase order number. Provide this or dscoOrderId or supplierOrderNumber to identify the order. |
| `supplierOrderNumber` | body | `string` | no | Supplier order number. Provide this or dscoOrderId or poNumber to identify the order. |
| `shipments[]` | body | `array<object>` | yes | Array of shipment objects to add to the order. |
| `shipments[].lineItems[]` | body | `array<object>` | yes | Line items included in the shipment. |
| `shipments[].trackingNumber` | body | `string` | yes | Carrier tracking number for the shipment. |
| `shipments[].lineItems[].quantity` | body | `number` | yes | Quantity of this line item included in the shipment. |
| `shipments[].shipDate` | body | `date` | no | Shipment date in ISO 8601 format. |
| `shipments[].lineItems[].lineNumber` | body | `number` | no | Order line number for the shipped item when needed to disambiguate the item. |
| `shipments[].lineItems[].sku` | body | `string` | no | SKU of the shipped item. One item identifier is required on each shipment line item. |
| `shipments[].shipCarrier` | body | `string` | no | Carrier name for the shipment. |
| `shipments[].shipMethod` | body | `string` | no | Shipping method for the shipment. |
| `shipments[].warehouseCode` | body | `string` | no | Warehouse code for the shipment. |
