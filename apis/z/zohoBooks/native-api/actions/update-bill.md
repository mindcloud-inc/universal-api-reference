# Update Bill with Zoho Books

## Endpoint

- **Method:** `PUT`
- **Path:** `/bills/:bill_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Update Bill](https://www.zoho.com/books/api/v3/bills/#update-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bill_id` | path | `string` | yes | Unique identifier of the bill. |
| `bill_number` | body | `string` | yes | Bill number. |
| `line_items[]` | body | `array<object>` | no | Line items of the bill. |
| `line_items[].account_id` | body | `string` | no | Expense account for the bill line item. |
| `line_items[].description` | body | `string` | no | Bill line item description. |
| `line_items[].line_item_id` | body | `string` | no | Existing bill line item identifier. |
| `line_items[].quantity` | body | `number` | no | Bill line item quantity. |
| `line_items[].rate` | body | `number` | no | Bill line item rate. |
| `notes` | body | `string` | no | Notes for the bill. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `reference_number` | body | `string` | no | Reference number. |
| `vendor_id` | body | `string` | yes | Vendor for the bill. |
