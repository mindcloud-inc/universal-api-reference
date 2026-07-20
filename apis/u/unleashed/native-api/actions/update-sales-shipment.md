# Update Sales Shipment with Unleashed

Updates an existing sales shipment in Unleashed.

## Endpoint

- **Method:** `PUT`
- **Path:** `/SalesShipments/:salesShipmentGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Update Sales Shipment](https://apidocs.unleashedsoftware.com/SalesShipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesShipmentGuid` | path | `string` | yes | The Unleashed sales shipment GUID. |
| `Guid` | body | `string` | yes | Unique identifier for the sales shipment. |
| `ShipmentStatus` | body | `string` | yes | Shipment status for the sales shipment. |
| `Comments` | body | `string` | no | Comments for the sales shipment. |
| `SalesShipmentLines[].Guid` | body | `string` | no | Existing shipment line GUID for updates. |
| `SalesShipmentLines[].Product.ProductCode` | body | `string` | yes | Product code for the sales shipment line. |
| `SalesShipmentLines[].ShipmentQty` | body | `number` | yes | Shipment quantity for the sales shipment line. |
| `SalesShipmentLines[].SalesOrderLineNumber` | body | `number` | yes | Sales order line number for the shipment line. |
