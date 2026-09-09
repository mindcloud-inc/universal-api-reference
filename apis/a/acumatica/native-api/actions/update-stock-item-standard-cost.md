# Update Stock Item Standard Cost with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/StockItem/UpdateStandardCostStockItem`
- **Base URL:** `{uRL}`
- **Official documentation:** [Update Stock Item Standard Cost](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity` | body | `object` | no |
| `entity.InventoryID` | body | `object` | no |
| `entity.InventoryID.value` | body | `string` | yes |
