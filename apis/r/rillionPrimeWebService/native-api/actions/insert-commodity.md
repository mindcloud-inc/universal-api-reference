# Insert Commodity with Rillion Prime Web Service

Insert a commodity into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Commodity` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Commodity section. |
| `Commodity.Commodity` | body | `string` | yes | The name of the commodity |
| `Commodity.RolePermission` | body | `string` | no | — |
| `Commodity.LinkToSupplier` | body | `string` | no | — |
| `Commodity.AdvisoryRole1` | body | `string` | no | — |
| `Commodity.AdvisoryRole2` | body | `string` | no | — |
| `Commodity.AdvisoryRole3` | body | `string` | no | — |
| `Commodity.ProductGroupName` | body | `string` | no | — |
| `Commodity.ItemFormName` | body | `string` | no | — |
| `Commodity.AvailableForFreetext` | body | `boolean` | no | — |
| `Commodity.CommodityCode` | body | `string` | no | CommodityCode |
| `Commodity.Company` | body | `list<string>` | no | Company that commodity is linked to |
| `Commodity.BuyersHelp` | body | `boolean` | no | ResponsiblePurchaseOrderRole inserted last in the flow: 0=No, 1=Yes |
| `Commodity.ResponsiblePurchaseOrderRole` | body | `string` | no | Responsible PurchaseOrderRole |
| `Commodity.PurchaseOrderMatchType` | body | `number` | no | PurchaseOrderMatchType 0=Number;1=Amount |
| `Commodity.Account` | body | `string` | no | Account |
| `Commodity.VatCode` | body | `string` | no | VAT Codes |
| `Commodity.ExpenditureAmount` | body | `number` | yes | Amount |
| `Commodity.Group1` | body | `string` | no | Free field of Type1 |
| `Commodity.Group2` | body | `string` | no | Free field of Type2 |
| `Commodity.Group3` | body | `string` | no | Free field of Type3 |
| `Commodity.ExternalId` | body | `string` | no | — |
| `Commodity.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
