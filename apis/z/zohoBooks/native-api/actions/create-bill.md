# Create Bill with Zoho Books

## Endpoint

- **Method:** `POST`
- **Path:** `/bills`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Create Bill](https://www.zoho.com/books/api/v3/bills/#create-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bill_number` | body | `string` | yes | Bill number. |
| `date` | body | `string` | no | Bill date. |
| `due_date` | body | `string` | no | Bill due date. |
| `line_items[]` | body | `array<object>` | no | Line items of the bill. |
| `line_items[].account_id` | body | `string` | no | Expense account for the bill line item. |
| `line_items[].description` | body | `string` | no | Bill line item description. |
| `line_items[].quantity` | body | `number` | no | Bill line item quantity. |
| `line_items[].rate` | body | `number` | no | Bill line item rate. |
| `notes` | body | `string` | no | Notes for the bill. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `reference_number` | body | `string` | no | Reference number. |
| `vendor_id` | body | `string` | yes | Vendor for the bill. |
