# Update Customer Payment with Zoho Books

## Endpoint

- **Method:** `PUT`
- **Path:** `/customerpayments/:payment_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Update Customer Payment](https://www.zoho.com/books/api/v3/customer-payments/#update-a-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Payment amount. |
| `amount_applied` | body | `number` | no | Top-level applied amount documented by Zoho for payment update. |
| `customer_id` | body | `string` | yes | Customer involved in the payment. |
| `date` | body | `string` | no | Payment date. |
| `description` | body | `string` | no | Payment description. |
| `invoice_id` | body | `string` | no | Top-level invoice identifier documented by Zoho for payment update. |
| `invoices[]` | body | `array<object>` | no | Invoices associated with the payment. |
| `invoices[].amount_applied` | body | `number` | no | Amount applied to the invoice inside the invoices array. |
| `invoices[].invoice_id` | body | `string` | no | Invoice identifier inside the invoices array. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `payment_id` | path | `string` | yes | Unique identifier of the payment. |
| `payment_mode` | body | `string` | yes | Payment mode. |
| `reference_number` | body | `string` | no | Reference number. |
