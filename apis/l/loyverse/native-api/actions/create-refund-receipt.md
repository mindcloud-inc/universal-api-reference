# Create Refund Receipt with Loyverse

Creates a refund receipt in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts/:receipt_number/refund`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create Refund Receipt](https://developer.loyverse.com/docs/#tag/Receipts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receipt_number` | path | `string` | yes | The sales receipt number for a refund |
| `receipt_date` | body | `date` | no | By default, it matches the created_at value (time when receipt was created on the Loyverse server). You can set receipt_date to the value that is equal to the date and time in the past when the refund was created in another system. |
| `source` | body | `string` | no | The name of the the source this receipt comes from. By default it is the name of the application that created the receipt. |
| `employee_id` | body | `string` | no | The employee id associated with the receipt |
| `store_id` | body | `string` | no | The store id associated with the refund receipt. By default, it matches the store id of the sales receipt. |
| `line_items[]` | body | `array<object>` | yes | The line items included in the refund |
