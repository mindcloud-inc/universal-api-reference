# Add Invoice Payment with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:urlKey/invoices/:invoice/payments`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Add Invoice Payment](https://www.refrens.com/api/docs/payment-updates/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invoice` | path | `string` | yes |
| `amount` | body | `number` | yes |
| `paymentDate` | body | `date` | yes |
| `paymentMethod` | body | `string` | yes |
