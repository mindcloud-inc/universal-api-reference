# Create Sales Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendinvoice`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Sales Invoice](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-sales-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer` | body | `object` | yes | Customer object, for example {"Id":"..."}. |
| `DocDate` | body | `string` | yes | Invoice date in Merit date string format. |
| `DueDate` | body | `string` | yes | Invoice due date in Merit date string format. |
| `InvoiceNo` | body | `string` | yes | Invoice number. |
| `InvoiceRow[]` | body | `array<object>` | yes | Array of invoice row objects. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of tax amount objects. |
| `TotalAmount` | body | `number` | yes | Invoice total amount. |
| `CurrencyCode` | body | `string` | no | Currency code, for example EUR. |
