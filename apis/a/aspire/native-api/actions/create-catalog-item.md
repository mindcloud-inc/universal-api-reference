# Create Catalog Item with Aspire

Creates a new catalog item in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `CatalogItems`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Catalog Item](https://cloud-api.youraspire.com/swagger/index.html#/CatalogItems/CatalogItems_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CatalogItemCategoryID` | body | `number` | yes |
| `ItemType` | body | `string` | yes |
| `ItemName` | body | `string` | no |
| `ItemAlternateName` | body | `string` | no |
| `ItemDescription` | body | `string` | no |
| `ItemCode` | body | `string` | no |
| `ItemCost` | body | `number` | no |
| `PurchaseUnitTypeID` | body | `number` | no |
| `AllocationUnitTypeID` | body | `number` | no |
| `UnitTypeAllocationConversion` | body | `number` | no |
| `EPANumber` | body | `string` | no |
| `EPAName` | body | `string` | no |
| `Inventory` | body | `boolean` | no |
| `AvailableToBid` | body | `boolean` | yes |
| `Active` | body | `boolean` | yes |
| `TakeoffItemID` | body | `number` | no |
| `PurchaseUnitCost` | body | `number` | no |
| `ForceUnitPricing` | body | `boolean` | no |
| `AllocateFromMobile` | body | `boolean` | no |
| `CatalogId` | body | `number` | no |
| `MaterialBarcode1` | body | `string` | no |
| `MaterialBarcode2` | body | `string` | no |
