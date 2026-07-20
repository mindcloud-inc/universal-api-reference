# List Inventory Stock Levels with Logiwa Legacy WMS

By using this endpoint, the users can obtain their current inventories based on the locations and also they may obtain some attributes such as Lot Number, and Expiration Date. The data obtained from this endpoint is raw data, the users may calculate the stock according to their logic.

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/GetAvailableStockInfo`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Inventory Stock Levels](https://developer.logiwa.com/?id=5ed03a00e6466c102c89922a)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `brand` | body | `string` | no |
| `itemGroup` | body | `string` | no |
| `location` | body | `string` | no |
| `lotNumber` | body | `string` | no |
| `warehouseID` | body | `string` | yes |
| `itemCode` | body | `string` | no |
| `depoID` | body | `string` | yes |
| `expirationDate` | body | `string` | no |
| `isDamaged` | body | `boolean` | no |
| `isLocked` | body | `boolean` | no |
| `isPickable` | body | `boolean` | no |
| `lastModifiedDate_End` | body | `string` | no |
| `lastModifiedDate_Start` | body | `string` | no |
| `locationZone` | body | `string` | no |
| `openToSales` | body | `boolean` | no |
| `packType` | body | `string` | no |
| `pickingType` | body | `string` | no |
| `productionDate` | body | `string` | no |
| `quarantineReason` | body | `string` | no |
| `stockReferenceNo` | body | `string` | no |
| `suitabilityReason` | body | `string` | no |
