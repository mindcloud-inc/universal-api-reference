# Create Purchase Invoice Waiting Approval with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendpurchorder`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Purchase Invoice Waiting Approval](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/create-purchase-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Vendor` | body | `object` | yes | Vendor object. |
| `DocDate` | body | `string` | yes | Document date in YYYYmmDD format. |
| `DueDate` | body | `string` | yes | Due date in YYYYmmDD format. |
| `BillNo` | body | `string` | yes | Bill number. |
| `ExpenseClaim` | body | `boolean` | no | Whether this purchase order is an expense claim. |
| `CurrencyCode` | body | `string` | no | Currency code. |
| `InvoiceRow[]` | body | `array<object>` | yes | Array of purchase order row objects. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of VAT amount objects. |
| `TotalAmount` | body | `number` | yes | Amount without VAT. |
| `TotalSum` | body | `number` | yes | Amount with VAT. |
