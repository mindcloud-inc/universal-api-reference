# Create Credit Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v1/sendinvoice`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Credit Invoice](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-credit-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer` | body | `object` | yes | Customer object, for example {"Id":"..."}. |
| `DocDate` | body | `string` | yes | Invoice date in Merit date string format. |
| `DueDate` | body | `string` | yes | Invoice due date in Merit date string format. |
| `InvoiceNo` | body | `string` | yes | Credit invoice number. |
| `InvoiceRow[]` | body | `array<object>` | yes | Array of invoice row objects with negative quantities for crediting. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of tax amount objects. |
| `TotalAmount` | body | `number` | yes | Credit invoice total amount. |
| `CurrencyCode` | body | `string` | no | Currency code, for example EUR. |
