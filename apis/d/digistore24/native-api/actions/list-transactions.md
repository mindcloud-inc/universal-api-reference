# List Transactions with Digistore24

Retrieves payments, returns, and chargebacks from Digistore24.

## Endpoint

- **Method:** `POST`
- **Path:** `/listTransactions`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [List Transactions](https://digistore24.com/api/docs/paths/listTransactions.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date/time |
| `to` | query | `string` | no | End date/time |
| `search` | query | `object` | no | Structured search filters |
| `search.role` | query | `string` | no | Filter by role |
| `search.product_id` | query | `string` | no | Filter by product ID |
| `search.first_name` | query | `string` | no | Filter by buyer first name |
| `search.last_name` | query | `string` | no | Filter by buyer last name |
| `search.email` | query | `string` | no | Filter by buyer email |
| `search.has_affiliate` | query | `boolean` | no | Filter transactions with or without affiliate |
| `search.affiliate_name` | query | `string` | no | Filter by affiliate name |
| `search.pay_method` | query | `string` | no | Filter by payment method |
| `search.billing_type` | query | `string` | no | Filter by billing type |
| `search.transaction_type` | query | `string` | no | Filter by transaction type |
| `search.currency` | query | `string` | no | Filter by currency code |
| `search.purchase_id` | query | `string` | no | Filter by purchase ID |
| `sort_by` | query | `string` | no | Sort transactions |
| `sort_order` | query | `string` | no | Sort order |
| `page_no` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Page size |
