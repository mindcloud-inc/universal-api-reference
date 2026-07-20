# List Payments with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getpayments`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [List Payments](https://api.merit.ee/connecting-robots/reference-manual/payments/list-of-payments/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PeriodStart` | body | `string` | yes |
| `PeriodEnd` | body | `string` | yes |
| `PaymentType` | body | `number` | no |
| `BankId` | body | `string` | no |
| `DateType` | body | `number` | yes |
