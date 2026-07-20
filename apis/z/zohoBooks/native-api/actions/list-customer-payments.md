# List Customer Payments with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/customerpayments`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Customer Payments](https://www.zoho.com/books/api/v3/customer-payments/#list-customer-payments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | query | `number` | no | Search payments by amount. |
| `customer_id` | query | `string` | no | Customer ID for the payment. |
| `customer_name` | query | `string` | no | Search payments by customer name. |
| `date` | query | `string` | no | Search payments by date. |
| `filter_by` | query | `string` | no | Filter payments by mode. |
| `notes` | query | `string` | no | Search payments by notes. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `payment_mode` | query | `string` | no | Search payments by payment mode. |
| `reference_number` | query | `string` | no | Search payments by reference number. |
| `search_text` | query | `string` | no | Search by reference number, customer name, or description. |
| `sort_column` | query | `string` | no | Sort payments by the selected column. |
