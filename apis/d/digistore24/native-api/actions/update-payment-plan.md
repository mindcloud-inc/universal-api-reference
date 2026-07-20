# Update Payment Plan with Digistore24

Updates an existing payment plan in Digistore24.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updatePaymentplan`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Update Payment Plan](https://digistore24.com/api/docs/paths/updatePaymentplan.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentplan_id` | query | `number` | yes | Payment plan ID |
| `first_amount` | body | `number` | no | First payment amount |
| `first_billing_interval` | body | `string` | no | First billing interval |
| `currency` | body | `string` | no | Currency code |
| `other_amounts` | body | `number` | no | Subsequent payment amount |
| `other_billing_intervals` | body | `string` | no | Subsequent billing interval |
| `number_of_installments` | body | `number` | no | Installment count |
| `is_active` | body | `boolean` | no | Payment plan active flag |
| `cancel_policy` | body | `string` | no | Cancellation policy |
