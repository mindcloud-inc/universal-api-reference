# Create Purchase Order with Zahara

Creates a new purchase order in Zahara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/{businessUnitApiKey}/PurchaseOrder/Add`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Create Purchase Order](https://ask.zaharasoftware.com/api-docs/add-purchase-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RequisitorId` | body | `number` | yes | Requisitor user ID. |
| `TotalNetValue` | body | `number` | yes | Purchase order total net value. |
| `TotalGrossValue` | body | `number` | yes | Purchase order total gross value. |
| `RequiredDate` | body | `date` | yes | Required delivery date. |
| `DocumentId` | body | `number` | yes | Document ID for create payloads, usually 0. |
| `BusinessDivisionId` | body | `number` | yes | Business division ID. |
| `SupplierId` | body | `number` | yes | Supplier ID. |
| `LineItems[]` | body | `array<object>` | yes | Purchase order line items. |
| `LineItems[0]` | body | `object` | yes | First purchase order line item object. |
| `CurrencyId` | body | `number` | yes | Currency ID. |
| `CustomFields[]` | body | `array<object>` | yes | Custom fields array. |
| `CustomFieldValues[]` | body | `array<object>` | yes | Custom field values array. |
| `LineItems[0].LineItemId` | body | `number` | yes | First line item ID, usually 0 for create. |
| `LineItems[0].DocumentId` | body | `number` | yes | First line item document ID, usually 0 for create. |
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
| `LineItems[0].QuantityReceived` | body | `number` | yes | Quantity received for the first line item. |
| `LineItems[0].DiscountPercentage` | body | `number` | yes | Discount percentage for the first line item. |
| `LineItems[0].DivisionId` | body | `number` | yes | Division ID for the first line item. |
| `LineItems[0].RequiredDate` | body | `date` | yes | Required date for the first line item. |
