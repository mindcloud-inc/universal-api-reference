# List Invoices with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Invoices](https://www.zoho.com/books/api/v3/invoices/#list-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `string` | no | Search invoices by customer ID. |
| `invoice_number` | query | `string` | no | Search invoices by invoice number. |
| `item_id` | query | `string` | no | Search invoices by item ID. |
| `status` | query | `list` | no | Search invoices by invoice status. Accepted values: `draft`, `overdue`, `paid`, `partially_paid`, `sent`, `unpaid`, `viewed`, `void`. |
| `date` | query | `date` | no | Search invoices by invoice date in yyyy-mm-dd format. |
| `due_date` | query | `date` | no | Search invoices by due date in yyyy-mm-dd format. |
| `search_text` | query | `string` | no | Search invoices by invoice number, purchase order, or customer name. |
| `sort_column` | query | `list` | no | Sort invoices by a supported column. Accepted values: `balance`, `created_time`, `customer_name`, `date`, `due_date`, `invoice_number`, `total`. |
