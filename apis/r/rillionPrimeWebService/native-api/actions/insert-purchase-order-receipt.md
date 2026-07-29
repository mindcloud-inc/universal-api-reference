# Insert Purchase Order Receipt with Rillion Prime Web Service

Insert a purchase order receipt in Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrderReceipt` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrderReceipt section. |
| `PurchaseOrderReceipt.Ean` | body | `string` | yes | EAN/GLN of the company to which the order belongs |
| `PurchaseOrderReceipt.PurchaseOrderNo` | body | `string` | yes | Order number |
| `PurchaseOrderReceipt.SupplierPurchaseOrderNo` | body | `string` | no | The supplier’s order number |
| `PurchaseOrderReceipt.PlannedDeliveryDate` | body | `date` | no | Planned delivery date |
| `PurchaseOrderReceipt.ConfirmedDeliveryDate` | body | `date` | no | Planned delivery date |
| `PurchaseOrderReceipt.Status` | body | `string` | no | Purchase order status: 2=Order confirmed (default); 3=Delivery notified |
