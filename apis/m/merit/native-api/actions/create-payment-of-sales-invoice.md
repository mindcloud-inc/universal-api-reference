# Create Payment Of Sales Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendpayment`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Payment Of Sales Invoice](https://api.merit.ee/connecting-robots/reference-manual/payments/create-payment/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `BankId` | body | `string` | no |
| `IBAN` | body | `string` | no |
| `CustomerName` | body | `string` | yes |
| `InvoiceNo` | body | `string` | yes |
| `PaymentDate` | body | `string` | yes |
| `RefNo` | body | `string` | no |
| `Amount` | body | `number` | yes |
| `CurrencyCode` | body | `string` | no |
| `CurrencyRate` | body | `number` | no |
