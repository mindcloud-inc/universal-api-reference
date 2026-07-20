# Create Payment Of Purchase Invoice with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendPaymentV`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Payment Of Purchase Invoice](https://api.merit.ee/connecting-robots/reference-manual/payments/payment-of-purchase-invoice/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `BankId` | body | `string` | no |
| `IBAN` | body | `string` | no |
| `VendorName` | body | `string` | yes |
| `BillNo` | body | `string` | yes |
| `PaymentDate` | body | `string` | yes |
| `RefNo` | body | `string` | no |
| `Amount` | body | `number` | yes |
| `CurrencyCode` | body | `string` | no |
| `CurrencyRate` | body | `number` | no |
