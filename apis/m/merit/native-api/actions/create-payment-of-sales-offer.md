# Create Payment Of Sales Offer with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendPaymentO`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Payment Of Sales Offer](https://api.merit.ee/connecting-robots/reference-manual/payments/create-payment-of-sales-offer/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `BankId` | body | `string` | no |
| `IBAN` | body | `string` | no |
| `CustomerName` | body | `string` | yes |
| `OfferNo` | body | `string` | yes |
| `PaymentDate` | body | `string` | yes |
| `RefNo` | body | `string` | no |
| `Amount` | body | `number` | yes |
| `CurrencyCode` | body | `string` | no |
| `CurrencyRate` | body | `number` | no |
