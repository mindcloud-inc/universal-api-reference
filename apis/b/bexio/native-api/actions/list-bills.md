# List Bills with Bexio

Retrieves bills from Bexio.

## Endpoint

- **Method:** `GET`
- **Path:** `/4.0/purchase/bills`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [List Bills](https://docs.bexio.com/#tag/Bills/operation/ApiBillsList_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Limit the number of results (max is 500). |
| `page` | query | `number` | no | Current page. |
| `order` | query | `list<string>` | no | Sorting order. Accepted values: `0`, `1`. |
| `sort` | query | `string` | no | Field to sort by. |
| `fields[]` | query | `array<string>` | no | Fields for which search will be run. |
| `search_term` | query | `string` | no | Term to search for. Minimum 3 characters, maximum 255 characters. |
| `status` | query | `list<string>` | no | Bill status filter. Accepted values: `0`, `1`, `2`, `3`. |
| `bill_date_start` | query | `date` | no | Earliest accepted bill date. |
| `bill_date_end` | query | `date` | no | Latest accepted bill date. |
| `due_date_start` | query | `date` | no | Earliest accepted due date. |
| `due_date_end` | query | `date` | no | Latest accepted due date. |
| `vendor_ref` | query | `string` | no | Filter for vendor reference. |
| `title` | query | `string` | no | Filter by bill title. |
| `currency_code` | query | `string` | no | Filter by currency code. |
| `pending_amount_min` | query | `number` | no | Minimum pending amount. |
| `pending_amount_max` | query | `number` | no | Maximum pending amount. |
| `vendor` | query | `string` | no | Vendor filter. |
| `gross_min` | query | `number` | no | Minimum gross amount. |
| `gross_max` | query | `number` | no | Maximum gross amount. |
| `net_min` | query | `number` | no | Minimum net amount. |
| `net_max` | query | `number` | no | Maximum net amount. |
| `document_no` | query | `string` | no | Filter by document number. |
| `supplier_id` | query | `number` | no | Filter by supplier ID. |
| `average_exchange_rate_enabled` | query | `boolean` | no | Filter by average exchange rate flag. |
