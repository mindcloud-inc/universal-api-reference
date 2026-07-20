# List Customer Payments with Zoho Invoice

Retrieves customer payments from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/customerpayments`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Customer Payments](https://www.zoho.com/invoice/api/v3/customer-payments/#list-customer-payments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `customer_name` | query | `string` | no | Search payments by customer name. Variants: customer_name_startswith and customer_name_contains. Maximum length [100] |
| `reference_number` | query | `string` | no | Search payments by reference number. Variants: reference_number_startswith and reference_number_contains. Maximum length [100] |
| `date` | query | `date` | no | Date on which payment is made. Date format yyyy-mm-dd. |
| `amount` | query | `number` | no | Search payments by payment amount. Variants: amount_less_than, amount_less_equals, amount_greater_than, amount_greater_equals. |
| `notes` | query | `string` | no | Search payments by customer notes. Variants: notes_startswith and notes_contains. |
| `payment_mode` | query | `string` | no | Search payments by payment mode. Variants: payment_mode_startswith and payment_mode_contains. |
| `filter_by` | query | `string` | no | Filter payments by mode. Accepted values: `options`. |
| `search_text` | query | `string` | no | Search payments by reference number, customer name, or payment description. Maximum length [100] |
