# Create Recurring Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendperinvoice`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Recurring Invoice](https://api.merit.ee/connecting-robots/reference-manual/recurring-invoices/create-recurring-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer` | body | `object` | yes | Customer object. |
| `StartDate` | body | `string` | yes | Recurring invoice start date in YYYYmmDD format. |
| `NextDate` | body | `string` | yes | Next invoice date in YYYYmmDD format. |
| `Cycle` | body | `number` | yes | 1 month, 2 quarter, 3 year, 4 week. |
| `Period` | body | `number` | yes | Invoice period mode. |
| `InvoiceRow[]` | body | `array<object>` | yes | Array of invoice row objects. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of VAT amount objects. |
| `TotalAmount` | body | `number` | yes | Total amount without VAT. |
| `TotalSum` | body | `number` | yes | Total amount including VAT. |
| `CurrencyCode` | body | `string` | no | Invoice currency code. |
| `Code` | body | `string` | no | Recurring invoice code. |
| `InvoiceNo` | body | `string` | no | Invoice number. |
| `HComment` | body | `string` | no | Header comment. |
| `FComment` | body | `string` | no | Footer comment. |
| `PaymentDay` | body | `number` | no | Payment day. |
| `ReferenceNo` | body | `string` | no | Reference number. |
| `PriceInclVat` | body | `boolean` | no | Whether prices include VAT. |
| `Payer` | body | `object` | no | Optional payer object. |
| `EndDate` | body | `string` | no | Recurring invoice end date in YYYYmmDD format. |
