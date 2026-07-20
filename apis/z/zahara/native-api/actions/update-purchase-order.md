# Update Purchase Order with Zahara

Updates an existing purchase order in Zahara.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/{businessUnitApiKey}/PurchaseOrder/Update/{{documentId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Update Purchase Order](https://ask.zaharasoftware.com/api-docs/update-purchase-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Purchase order document ID to update. |
| `LineItems[0]` | body | `object` | yes | First purchase order line item object. |
| `RequisitorId` | body | `number` | yes | Requisitor user ID. |
| `TotalNetValue` | body | `number` | yes | Purchase order total net value. |
| `TotalGrossValue` | body | `number` | yes | Purchase order total gross value. |
| `RequiredDate` | body | `date` | yes | Required delivery date. |
| `DocumentId` | body | `number` | yes | Document ID echoed in the update body. |
| `BusinessDivisionId` | body | `number` | yes | Business division ID. |
| `SupplierId` | body | `number` | yes | Supplier ID. |
| `CurrencyId` | body | `number` | yes | Currency ID. |
| `LineItems[0].ProjectId` | body | `number` | yes | Project ID for the first line item. |
| `LineItems[0].CostCodeId` | body | `number` | yes | Cost code ID for the first line item. |
| `LineItems[0].Quantity` | body | `number` | yes | Quantity for the first line item. |
| `LineItems[0].Price` | body | `number` | yes | Price for the first line item. |
| `LineItems[0].Description` | body | `string` | yes | Description for the first line item. |
| `LineItems[0].NominalCodeId` | body | `number` | yes | Nominal code ID for the first line item. |
| `LineItems[0].TaxCodeId` | body | `number` | yes | Tax code ID for the first line item. |
| `LineItems[0].TaxPercentage` | body | `number` | yes | Tax percentage for the first line item. |
| `LineItems[0].TaxValue` | body | `number` | yes | Tax value for the first line item. |
| `LineItems[0].NetValue` | body | `number` | yes | Net value for the first line item. |
| `LineItems[0].DivisionId` | body | `number` | yes | Division ID for the first line item. |
| `LineItems[0].RequiredDate` | body | `date` | yes | Required date for the first line item. |
