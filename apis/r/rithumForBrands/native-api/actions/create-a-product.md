# Create a Product with Rithum for Brands

## Endpoint

- **Method:** `POST`
- **Path:** `Products`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Create a Product](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=1bdc17c52fd15994cffb5ff62799b6e9)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ProfileID` | body | `list<number>` | yes |
| `Sku` | body | `string` | yes |
| `Title` | body | `string` | yes |
| `ASIN` | body | `string` | no |
| `ShortDescription` | body | `string` | no |
| `Height` | body | `number` | no |
| `Length` | body | `number` | no |
| `Width` | body | `number` | no |
| `Weight` | body | `number` | no |
| `StoreTitle` | body | `string` | no |
| `Brand` | body | `string` | no |
| `Manufacturer` | body | `string` | no |
| `MPN` | body | `string` | no |
| `Condition` | body | `string` | no |
| `Description` | body | `string` | no |
| `UPC` | body | `string` | no |
| `ParentSku` | body | `string` | no |
| `BuyItNowPrice` | body | `number` | no |
| `RetailPrice` | body | `number` | no |
| `IsParent` | body | `boolean` | no |
| `IsInRelationship` | body | `boolean` | no |
| `ParentProductID` | body | `number` | no |
| `Condition` | body | `string` | no |
| `WarehouseLocation` | body | `string` | no |
| `RelationshipName` | body | `string` | no |
