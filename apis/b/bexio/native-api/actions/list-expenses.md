# List Expenses with Bexio

Retrieves expenses from Bexio.

## Endpoint

- **Method:** `GET`
- **Path:** `/4.0/expenses`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [List Expenses](https://docs.bexio.com/#tag/Expenses/operation/ApiExpensesList_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `page` | query | `number` | no | — |
| `order` | query | `list<string>` | no | Accepted values: `0`, `1`. |
| `sort` | query | `string` | no | — |
| `vendor` | query | `string` | no | — |
| `gross_min` | query | `number` | no | — |
| `gross_max` | query | `number` | no | — |
| `net_min` | query | `number` | no | — |
| `net_max` | query | `number` | no | — |
| `paid_on_start` | query | `date` | no | — |
| `paid_on_end` | query | `date` | no | — |
| `created_at_start` | query | `date` | no | — |
| `created_at_end` | query | `date` | no | — |
| `title` | query | `string` | no | — |
| `currency_code` | query | `string` | no | — |
| `document_no` | query | `string` | no | — |
| `supplier_id` | query | `number` | no | — |
| `project_id` | query | `string` | no | — |
