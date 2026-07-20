# List Shipment Info - Import with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/ShipmentReportAllSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `WarehouseOrderID` | body | `number` | no |
| `WarehouseOrderCode` | body | `string` | no |
| `InventorySiteID` | body | `number` | no |
| `DepositorID` | body | `number` | no |
| `WarehouseID` | body | `number` | no |
| `ShipmentDateTime_Start` | body | `string` | no |
| `ShipmentDateTime_End` | body | `string` | no |
| `SSCC` | body | `string` | no |
| `WarehouseOrderTypeID` | body | `number` | no |
| `LocationCode` | body | `string` | no |
| `InventoryItemID` | body | `number` | no |
| `LotBatchNo` | body | `string` | no |
| `CarrierID` | body | `number` | no |
| `ChannelOrderCode` | body | `string` | no |
| `CarrierTrackingNumber` | body | `string` | no |
| `OrderDate_Start` | body | `string` | no |
| `OrderDate_End` | body | `string` | no |
| `channelID` | body | `number` | no |
| `StoreName` | body | `string` | no |
| `Country` | body | `string` | no |
| `State` | body | `string` | no |
| `City` | body | `string` | no |
| `CarrierAddressType` | body | `string` | no |
| `ItemCode` | body | `string` | no |
| `ItemDescription` | body | `string` | no |
| `snapshotDatetimeStart` | body | `string` | no |
| `snapshotDatetimeEnd` | body | `string` | no |
| `IsExported` | body | `boolean` | no |
| `PageSize` | body | `number` | no |
| `SelectedPageIndex` | body | `number` | no |
