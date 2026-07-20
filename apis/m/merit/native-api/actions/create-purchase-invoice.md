# Create Purchase Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendpurchinvoice`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Purchase Invoice](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/create-purchase-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Vendor` | body | `object` | yes | Vendor object. |
| `DocDate` | body | `string` | yes | Document date in YYYYmmDD format. |
| `DueDate` | body | `string` | yes | Due date in YYYYmmDD format. |
| `BillNo` | body | `string` | yes | Bill number. |
| `CurrencyCode` | body | `string` | no | Currency code. |
| `InvoiceRow[]` | body | `array<object>` | yes | Array of purchase invoice row objects. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of VAT amount objects. |
| `TotalAmount` | body | `number` | yes | Amount without VAT. |
| `TotalSum` | body | `number` | yes | Amount with VAT. |
| `RefNo` | body | `string` | no | Reference number. |
