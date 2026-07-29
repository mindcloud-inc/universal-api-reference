# List Commodities with Rillion Prime Web Service

List commodities in Rillion Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CommoditySelectParams` | body | `object` | no | Optional search filters. Leave everything empty to list all. |
| `CommoditySelectParams.Commodity` | body | `string` | no | Commodity name to match. |
| `CommoditySelectParams.Company` | body | `list<string>` | no | Company to scope the search. |
| `CommoditySelectParams.Supplier` | body | `string` | no | Supplier name. |
| `CommoditySelectParams.MaxNoOfResultRows` | body | `number` | no | Maximum number of commodities to return. |
| `CommoditySelectParams.CommodityID` | body | `string` | no | — |
| `CommoditySelectParams.CommodityCode` | body | `string` | no | — |
| `CommoditySelectParams.ItemFormName` | body | `string` | no | — |
| `CommoditySelectParams.ResponsiblePurchaseOrderRole` | body | `string` | no | — |
| `CommoditySelectParams.AdviserRole1` | body | `string` | no | — |
| `CommoditySelectParams.AdviserRole2` | body | `string` | no | — |
| `CommoditySelectParams.AdviserRole3` | body | `string` | no | — |
| `CommoditySelectParams.Group1` | body | `string` | no | — |
| `CommoditySelectParams.Group2` | body | `string` | no | — |
| `CommoditySelectParams.Group3` | body | `string` | no | — |
| `CommoditySelectParams.Role` | body | `string` | no | — |
| `CommoditySelectParams.SupplierID` | body | `number` | no | — |
| `CommoditySelectParams.CountSupplier` | body | `boolean` | no | — |
| `CommoditySelectParams.AvailableForFreetext` | body | `string` | no | — |
| `CommoditySelectParams.CompanyIsNull` | body | `boolean` | no | — |
| `CommoditySelectParams.ExpenditureID` | body | `number` | no | — |
