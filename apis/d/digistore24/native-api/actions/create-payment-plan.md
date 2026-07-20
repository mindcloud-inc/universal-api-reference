# Create Payment Plan with Digistore24

Creates a new payment plan in Digistore24.

## Endpoint

- **Method:** `POST`
- **Path:** `/createPaymentplan`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Create Payment Plan](https://digistore24.com/api/docs/paths/createPaymentplan.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | query | `string` | yes | Product ID |
| `data` | query | `object` | yes | Payment plan properties object |
| `data.first_amount` | query | `number` | no | Amount of first payment |
| `data.first_billing_interval` | query | `string` | no | Interval between purchase and second payment |
| `data.currency` | query | `string` | no | Three-character currency code |
| `data.other_amounts` | query | `number` | no | Amount for follow-up payments |
| `data.other_billing_intervals` | query | `string` | no | Interval for follow-up payments |
| `data.number_of_installments` | query | `number` | no | Number of installments |
| `data.is_active` | query | `boolean` | no | Whether the payment plan is active |
| `data.cancel_policy` | query | `string` | no | Minimum term policy |
