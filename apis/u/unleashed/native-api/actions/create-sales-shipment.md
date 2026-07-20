# Create Sales Shipment with Unleashed

Creates a new sales shipment in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/SalesShipments`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Create Sales Shipment](https://apidocs.unleashedsoftware.com/SalesShipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Guid` | body | `string` | yes | Unique identifier for the sales shipment. |
| `OrderNumber` | body | `string` | yes | Order number for the sales shipment. |
| `ShipmentStatus` | body | `string` | yes | Shipment status for the sales shipment. |
| `SalesShipmentLines[].Product.ProductCode` | body | `string` | yes | Product code for the sales shipment line. |
| `SalesShipmentLines[].ShipmentQty` | body | `number` | yes | Shipment quantity for the sales shipment line. |
| `SalesShipmentLines[].SalesOrderLineNumber` | body | `number` | yes | Sales order line number for the shipment line. |
