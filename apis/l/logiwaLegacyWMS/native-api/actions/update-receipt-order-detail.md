# Update Receipt Order Detail with Logiwa Legacy WMS

By using this endpoint, users can UPDATE the details of receipt orders if the ID field exists in the endpoint request. 

Users can CREATE receipt order details unless the Warehouse Receipt Order Detail ID is not added to the request.

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/WarehouseReceiptDetailUpdate`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [Update Receipt Order Detail](https://developer.logiwa.com/?id=62c7ce4be6466c3080236a04)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Code` | body | `string` | no |
| `ExpireDate` | body | `string` | no |
| `FreeAttr1` | body | `string` | no |
| `FreeAttr2` | body | `string` | no |
| `FreeAttr3` | body | `string` | no |
| `ID` | body | `number` | no |
| `InventoryItemID` | body | `number` | yes |
| `InventoryItemPackTypeDescription` | body | `string` | no |
| `InventoryItemPackTypeID` | body | `number` | yes |
| `LotBatchNo` | body | `string` | no |
| `Notes2` | body | `string` | no |
| `PlannedCUQuantity` | body | `number` | yes |
| `PlannedPackQuantity` | body | `number` | yes |
| `ProductionDate` | body | `string` | no |
| `SSCC` | body | `string` | no |
| `WarehouseReceiptID` | body | `number` | yes |
