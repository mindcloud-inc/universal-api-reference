# Get Receipt Report with Logiwa Legacy WMS

By using this endpoint, the users can obtain the receipt records.

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/ReceiptAllSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [Get Receipt Report](https://developer.logiwa.com/?id=5f7c281ce6466c3884d36b24)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InventorySiteID` | body | `string` | no | ID of inventory site. |
| `WarehouseID` | body | `string` | no | Id of the warehouse that receives receipt order |
| `DepositorID` | body | `string` | no | Id of depositor (client) who owns the inventory item to be received |
| `WarehouseReceiptID` | body | `string` | no | Id of receipt if the receipt order is received. ( Use List Receipt Orders to obtain this value ) |
| `InventoryItemID` | body | `string` | no | Id of inventory item received or will be received. ( Use Get Item ID ) |
| `ReferanceNo` | body | `string` | no | Reference number |
| `IsReturn` | body | `boolean` | no | If yes, the receive order is created for return operation. |
| `ReceiptDateTime_Start` | body | `date` | no | ReceiptDateTime_Start |
| `ReceiptDateTime_End` | body | `date` | no | ReceiptDateTime_End |
| `freeAttr3` | body | `string` | no | — |
