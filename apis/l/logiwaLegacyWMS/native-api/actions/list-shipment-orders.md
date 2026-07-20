# List Shipment Orders with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/WarehouseOrderSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Shipment Orders](https://developer.logiwa.com/?id=5df0db0be6466c2eec992f4b)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ID` | body | `string` | no |
| `Code` | body | `string` | no |
| `PriorityID` | body | `string` | no |
| `CustomerRefCode` | body | `string` | no |
| `DepositorRefCode` | body | `string` | no |
| `CustomerOrderNo` | body | `string` | no |
| `DepositorOrderNo` | body | `string` | no |
| `WarehouseOrderStatusID` | body | `string` | no |
| `CustomerID` | body | `number` | no |
| `CustomerCode` | body | `string` | no |
| `CustomerDescription` | body | `string` | no |
| `InventorySiteID` | body | `string` | no |
| `InventorySiteCode` | body | `string` | no |
| `WarehouseID` | body | `number` | no |
| `WarehouseCode` | body | `string` | no |
| `WarehouseDescription` | body | `string` | no |
| `DepositorID` | body | `number` | no |
| `DepositorCode` | body | `string` | no |
| `DepositorDescription` | body | `string` | no |
| `IsPrintCarrierLabelPackListAsLabel` | body | `boolean` | no |
| `CarrierTrackingNumber` | body | `string` | no |
| `OrderDate` | body | `string` | no |
| `PlannedDeliveryDate_Start` | body | `string` | no |
| `PlannedDeliveryDate_End` | body | `string` | no |
| `PlannedShipDate_Start` | body | `string` | no |
| `PlannedShipDate_End` | body | `string` | no |
| `LastModifiedDate_Start` | body | `string` | no |
| `LastModifiedDate_End` | body | `string` | no |
| `Notes` | body | `string` | no |
| `BusinessDaysInTransit` | body | `string` | no |
| `CustomerEmail` | body | `string` | no |
| `IsPrintCarrierLabelPackListOnSamePage` | body | `boolean` | no |
| `WarehouseOrderTypeID` | body | `string` | no |
| `WarehouseOrderTypeCode` | body | `string` | no |
| `CancellationDate_Start` | body | `string` | no |
| `CancellationDate_End` | body | `string` | no |
| `IsDocumentExist` | body | `boolean` | no |
| `PurchaseOrderID` | body | `string` | no |
| `PurchaseOrderCode` | body | `string` | no |
| `IsBackorder` | body | `boolean` | no |
| `NofShipmentLabel` | body | `string` | no |
| `IsAllocated` | body | `boolean` | no |
| `IsPickingStarted` | body | `boolean` | no |
| `IsPickingCompleted` | body | `boolean` | no |
| `ChannelID` | body | `string` | no |
| `ChannelDescription` | body | `string` | no |
| `CarrierID` | body | `string` | no |
| `CarrierDescription` | body | `string` | no |
| `CarrierShippingOptionsID` | body | `string` | no |
| `NofProducts` | body | `string` | no |
| `StoreName` | body | `string` | no |
| `LinkedChannelID` | body | `string` | no |
| `LinkedChannelDescription` | body | `string` | no |
| `BackWarehouseOrderID` | body | `string` | no |
| `BackWarehouseOrderCode` | body | `string` | no |
| `DropShipMasterOrderID` | body | `string` | no |
| `DropShipWarehouseOrderCode` | body | `string` | no |
| `DropShipNotes` | body | `string` | no |
| `ChannelOrderCode` | body | `string` | no |
| `WarehouseOrderOperationStatus` | body | `string` | no |
| `CarrierBillingTypeID` | body | `string` | no |
| `CarrierBillingTypeDescription` | body | `string` | no |
| `Driver` | body | `string` | no |
| `TaxesandDutiesBillingType` | body | `string` | no |
| `TaxandDutiesPayorInfo` | body | `string` | no |
| `methodName` | path | `list<string>` | no |
| `IsGetOrderDetails` | body | `boolean` | no |
| `IsGetCustomerAddressInfo` | body | `boolean` | no |
