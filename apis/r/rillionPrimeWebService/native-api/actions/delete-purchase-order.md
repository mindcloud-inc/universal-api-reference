# Delete Purchase Order with Rillion Prime Web Service

Delete a purchase order from Prime. Undocumented in the vendor guide — confirm semantics with Rillion before production use.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrder` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrder section. |
| `PurchaseOrder.Company` | body | `list<string>` | yes | Company to which the orderline belongs (FK to purchase order line) |
| `PurchaseOrder.PurchaseOrderNo` | body | `string` | yes | Order number (FK to purchase order line) |
| `PurchaseOrder.PurchaseOrderMatchType` | body | `number` | yes | Type of matching: 0=Quantity matching (set by default by the system), 1=Amount matching. |
| `PurchaseOrder.Status` | body | `number` | no | Purchase order status: 0=Created; 1=Ordered; 2=Order confirmed; 3=Delivery notified |
| `PurchaseOrder.PurchaseDate` | body | `date` | no | Order date |
| `PurchaseOrder.Supplier` | body | `string` | yes | Supplier |
| `PurchaseOrder.SupplierPurchaseOrderNo` | body | `string` | no | The supplier’s order number |
| `PurchaseOrder.Currency` | body | `string` | yes | Currency |
| `PurchaseOrder.Reference1` | body | `string` | no | Reference of type 1 |
| `PurchaseOrder.Reference2` | body | `string` | no | Reference of type 2 |
| `PurchaseOrder.PlannedDeliveryDate` | body | `date` | no | Planned delivery date |
| `PurchaseOrder.PlannedPaymentDueDate` | body | `date` | no | Planned payment date |
| `PurchaseOrder.HeaderText` | body | `string` | no | Free text printed out on purchase order |
| `PurchaseOrder.Note` | body | `string` | no | Free text |
| `PurchaseOrder.InvoiceSeries` | body | `string` | no | Invoice series |
| `PurchaseOrder.InvoiceNo` | body | `number` | no | Invoice number |
| `PurchaseOrder.Remove` | body | `number` | no | Is the record to be deleted: 0=No; 1=Yes |
| `PurchaseOrder.ResponsiblePurchaseOrderEmail` | body | `string` | no | E-mail adress to responsible purchaser |
| `PurchaseOrder.AutoDelivery` | body | `boolean` | no | AutoDelivery: 1=Delivery automatically created |
| `PurchaseOrder.Group1` | body | `string` | no | Free group 1 |
| `PurchaseOrder.Group2` | body | `string` | no | Free group 2 |
| `PurchaseOrder.Group3` | body | `string` | no | Free group 3 |
| `PurchaseOrder.ValidTo` | body | `date` | no | Valid to date for PurchaseOrder. |
| `PurchaseOrder.PurchaseOrderLine[]` | body | `array<object>` | no | Purchase Order Line lines. |
| `PurchaseOrder.PurchaseOrderLine[].Company` | body | `list<string>` | yes | Company to which the orderline belongs (FK to purchase order line) |
| `PurchaseOrder.PurchaseOrderLine[].PurchaseOrderNo` | body | `string` | yes | Order number (FK to purchase order line) |
| `PurchaseOrder.PurchaseOrderLine[].LineNo` | body | `string` | yes | Line number (FK to purchase order line) |
| `PurchaseOrder.PurchaseOrderLine[].FullyDelivered` | body | `number` | no | Set the purchase order line status to fully delivered: 0=No, 1=Yes |
| `PurchaseOrder.PurchaseOrderLine[].FullyInvoiced` | body | `number` | no | Set the purchase order line status to fully invoiced: 0=No, 1=Yes |
| `PurchaseOrder.PurchaseOrderLine[].YourReference` | body | `string` | no | Your reference |
| `PurchaseOrder.PurchaseOrderLine[].GoodsLabel` | body | `string` | no | Goods labelling |
| `PurchaseOrder.PurchaseOrderLine[].Item` | body | `string` | yes | Item |
| `PurchaseOrder.PurchaseOrderLine[].Description` | body | `string` | no | Description |
| `PurchaseOrder.PurchaseOrderLine[].Attribute` | body | `string` | no | Attribute |
| `PurchaseOrder.PurchaseOrderLine[].Number` | body | `number` | yes | Quantity |
| `PurchaseOrder.PurchaseOrderLine[].Unit` | body | `string` | no | Unit |
| `PurchaseOrder.PurchaseOrderLine[].Price` | body | `number` | yes | Unit price |
| `PurchaseOrder.PurchaseOrderLine[].Amount` | body | `number` | yes | Line amount |
| `PurchaseOrder.PurchaseOrderLine[].Discount` | body | `number` | yes | Discount in % |
| `PurchaseOrder.PurchaseOrderLine[].SupplierItem` | body | `string` | no | Supplier’s item number |
| `PurchaseOrder.PurchaseOrderLine[].PlannedDeliveryDate` | body | `date` | no | Planned delivery date |
| `PurchaseOrder.PurchaseOrderLine[].Note` | body | `string` | no | Free text |
| `PurchaseOrder.PurchaseOrderLine[].DeliveryNote` | body | `string` | no | — |
| `PurchaseOrder.PurchaseOrderLine[].InvoicedNumber` | body | `number` | no | Quantity of the order already matched to an invoice in the ERP system. |
| `PurchaseOrder.PurchaseOrderLine[].InvoicedPrice` | body | `number` | no | Price of the order already matched to an invoice in the ERP system. |
| `PurchaseOrder.PurchaseOrderLine[].InvoicedAmount` | body | `number` | no | Amount of the order already matched to an invoice in the ERP system. |
| `PurchaseOrder.PurchaseOrderLine[].InvoiceSeries` | body | `string` | no | Invoice series |
| `PurchaseOrder.PurchaseOrderLine[].InvoiceNo` | body | `number` | no | Invoice number |
| `PurchaseOrder.PurchaseOrderLine[].InvoiceStatus` | body | `number` | no | — |
| `PurchaseOrder.PurchaseOrderLine[].Remove` | body | `number` | no | Is the record to be deleted: 0=No; 1=Yes |
| `PurchaseOrder.PurchaseOrderLine[].Group1` | body | `string` | no | Free group 1 |
| `PurchaseOrder.PurchaseOrderLine[].Group2` | body | `string` | no | Free group 2 |
| `PurchaseOrder.PurchaseOrderLine[].Group3` | body | `string` | no | Free group 3 |
| `PurchaseOrder.PurchaseOrderLine[].ExternalId` | body | `string` | no | — |
| `PurchaseOrder.PurchaseOrderLine[].ExternalSource` | body | `string` | no | — |
| `PurchaseOrder.ExternalId` | body | `string` | no | — |
| `PurchaseOrder.ExternalSource` | body | `string` | no | — |
| `PurchaseOrder.CurrencyExternalId` | body | `string` | no | — |
| `PurchaseOrder.CurrencyExternalSource` | body | `string` | no | — |
| `PurchaseOrder.SupplierExternalId` | body | `string` | no | — |
| `PurchaseOrder.SupplierExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the deletion from the queue immediately. |
