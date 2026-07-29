# Insert Purchase Order Delivery with Rillion Prime Web Service

Register a delivery against a purchase order in Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrderDelivery` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrderDelivery section. |
| `PurchaseOrderDelivery.Company` | body | `list<string>` | yes | Company |
| `PurchaseOrderDelivery.Supplier` | body | `string` | yes | Supplier |
| `PurchaseOrderDelivery.SupplierDeliveryNote` | body | `string` | yes | Goods reciept number on the delivery reciept (can be used in PO matching) |
| `PurchaseOrderDelivery.DeliveryNote` | body | `string` | no | Delivery slip |
| `PurchaseOrderDelivery.DeliveryDate` | body | `date` | yes | Delivery date |
| `PurchaseOrderDelivery.Note` | body | `string` | no | Free text |
| `PurchaseOrderDelivery.Group1` | body | `string` | no | Free group 1 |
| `PurchaseOrderDelivery.Group2` | body | `string` | no | Free group 2 |
| `PurchaseOrderDelivery.Group3` | body | `string` | no | Free group 3 |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[]` | body | `array<object>` | no | Purchase Order Delivery Line lines. |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].PurchaseOrderNo` | body | `string` | yes | Order number |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].LineNo` | body | `string` | yes | Order line number |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Number` | body | `number` | yes | Quantity delivered |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Amount` | body | `number` | no | Amount delivered |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Note` | body | `string` | no | Free text |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Group1` | body | `string` | no | Free group 1 |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Group2` | body | `string` | no | Free group 2 |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].Group3` | body | `string` | no | Free group 3 |
| `PurchaseOrderDelivery.PurchaseOrderDeliveryLine[].SubDelivery` | body | `string` | no | Partial delivery id to purchase order line. |
| `PurchaseOrderDelivery.ExternalId` | body | `string` | no | — |
| `PurchaseOrderDelivery.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
