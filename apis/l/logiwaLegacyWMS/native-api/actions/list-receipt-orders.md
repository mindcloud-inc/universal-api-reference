# List Receipt Orders with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/WarehouseReceiptSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Receipt Orders](https://developer.logiwa.com/?id=5df0dcafe6466c2eec992f67)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | body | `number` | no | — |
| `Code` | body | `string` | no | — |
| `WarehouseID` | body | `number` | no | — |
| `DepositorID` | body | `number` | no | — |
| `InventorySiteID` | body | `number` | no | — |
| `PurchaseOrderID` | body | `string` | no | — |
| `InventorySiteDescription` | body | `string` | no | — |
| `IsGetOrderDetails` | body | `boolean` | no | — |
| `IntegrationKey` | body | `string` | no | — |
| `WarehouseReceiptTypeDescription` | body | `string` | no | — |
| `WarehouseReceiptStatusID` | body | `array<number>` | no | — |
| `WarehouseReceiptStatusDescription` | body | `string` | no | — |
| `WarehouseReceiptTypeID` | body | `string` | no | — |
| `WarehouseReceiptTypeDescription` | body | `string` | no | The `WarehouseReceiptTypeDescription`  Example 'Return' |
| `ReceiptDate` | body | `date` | no | — |
| `ReceiptDate_Start` | body | `date` | no | — |
| `ReceiptDate_End` | body | `date` | no | — |
| `ActualArrivalDate` | body | `date` | no | — |
| `ActualArrivalDate_Start` | body | `date` | no | — |
| `ActualArrivalDate_End` | body | `date` | no | — |
| `LastModifiedDate` | body | `date` | no | — |
| `LastModifiedDate_Start` | body | `date` | no | — |
| `LastModifiedDate_End` | body | `date` | no | — |
