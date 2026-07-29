# List Items with Rillion Prime Web Service

List purchasing items in Rillion Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ItemSelectParams` | body | `object` | no | Optional search filters. Leave everything empty to list all. |
| `ItemSelectParams.SearchAll` | body | `string` | no | Free-text search across the item catalog. |
| `ItemSelectParams.Company` | body | `list<string>` | no | Company to scope the search. |
| `ItemSelectParams.Supplier` | body | `string` | no | Supplier ID. |
| `ItemSelectParams.Description` | body | `string` | no | Match on item description. |
| `ItemSelectParams.OnlyInCatalogue` | body | `boolean` | no | Only items in the catalogue. |
| `ItemSelectParams.MaxNoOfResultRows` | body | `number` | no | Maximum number of items to return. |
| `ItemSelectParams.SupplierName` | body | `string` | no | — |
| `ItemSelectParams.Item` | body | `string` | no | Item identifier. |
| `ItemSelectParams.ItemID` | body | `string` | no | — |
| `ItemSelectParams.ItemCatalogue` | body | `string` | no | — |
| `ItemSelectParams.Note` | body | `string` | no | — |
| `ItemSelectParams.SupplierItem` | body | `string` | no | — |
| `ItemSelectParams.ResponsiblePurchaseOrderRole` | body | `string` | no | — |
| `ItemSelectParams.Commodity` | body | `string` | no | — |
| `ItemSelectParams.CommodityCode` | body | `string` | no | — |
| `ItemSelectParams.Manufacturer` | body | `string` | no | — |
| `ItemSelectParams.ManufacturerItem` | body | `string` | no | — |
| `ItemSelectParams.ContractNo` | body | `string` | no | — |
| `ItemSelectParams.Blocked` | body | `string` | no | — |
| `ItemSelectParams.BestBuy` | body | `string` | no | — |
| `ItemSelectParams.ValidFrom` | body | `date` | no | — |
| `ItemSelectParams.ValidTo` | body | `date` | no | — |
| `ItemSelectParams.Group1` | body | `string` | no | — |
| `ItemSelectParams.Group2` | body | `string` | no | — |
| `ItemSelectParams.Group3` | body | `string` | no | — |
| `ItemSelectParams.ExternalId` | body | `string` | no | — |
| `ItemSelectParams.ExternalSource` | body | `string` | no | — |
| `ItemSelectParams.OnlyFavourite` | body | `boolean` | no | — |
| `ItemSelectParams.OnlyBestBuy` | body | `boolean` | no | — |
| `ItemSelectParams.OnlyHaveContract` | body | `boolean` | no | — |
| `ItemSelectParams.OnlyEcoLabel` | body | `boolean` | no | — |
| `ItemSelectParams.FilterByPrice` | body | `boolean` | no | — |
| `ItemSelectParams.FilterByPriceMin` | body | `number` | no | — |
| `ItemSelectParams.FilterByPriceMax` | body | `number` | no | — |
| `ItemSelectParams.CompanyIsNull` | body | `boolean` | no | — |
| `ItemSelectParams.ExpenditureId` | body | `number` | no | — |
| `ItemSelectParams.ItemFormName` | body | `string` | no | — |
| `ItemSelectParams.ItemTypeLinksFrom` | body | `number` | no | — |
| `ItemSelectParams.ItemTypeLinksTo` | body | `number` | no | — |
