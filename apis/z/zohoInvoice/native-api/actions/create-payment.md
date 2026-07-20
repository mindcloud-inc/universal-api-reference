# Create Payment with Zoho Invoice

Creates a payment in Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/customerpayments`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Create Payment](https://www.zoho.com/invoice/api/v3/customer-payments/#create-a-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | Unique identifier of the organization. |
| `customer_id` | body | `string` | yes | Customer ID of the customer for whom the payment is recorded. |
| `payment_mode` | body | `string` | yes | Mode of payment. |
| `amount` | body | `number` | yes | Amount received in the payment. |
| `date` | body | `date` | yes | Date on which the payment is made. |
| `reference_number` | body | `string` | no | Reference number for the payment. |
| `description` | body | `string` | no | Description of the payment. |
| `invoices[]` | body | `array<object>` | yes | Invoices associated with the payment. |
| `invoices[].invoice_id` | body | `string` | yes | Invoice ID of the required invoice. |
| `invoices[].amount_applied` | body | `number` | yes | Amount paid for the invoice. |
| `exchange_rate` | body | `number` | no | Exchange rate for the currency used in the invoices and the customer's currency. |
| `payment_form` | body | `string` | no | Mode of vendor payment. |
| `bank_charges` | body | `number` | no | Additional bank charges. |
| `custom_fields[]` | body | `array<object>` | no | Custom fields for the payment. |
| `custom_fields[].label` | body | `string` | no | Name of the custom field. |
| `custom_fields[].value` | body | `string` | no | Value of the custom field. |
