# Create Sales Receipt with Loyverse

Creates a new sales receipt in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create Sales Receipt](https://developer.loyverse.com/docs/#tag/Receipts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_id` | body | `string` | yes | The store id associated with the receipt |
| `employee_id` | body | `string` | no | The employee id associated with the receipt |
| `order` | body | `string` | no | The order name or number associated with the receipt |
| `customer_id` | body | `string` | no | The customer id associated with the receipt |
| `source` | body | `string` | no | The name of the the source this receipt comes from. By default it is the name of the application that created the receipt. For receipts created from Loyverse mobile point of sale application the value is "point of sale". |
| `receipt_date` | body | `date` | no | By default, it matches the created_at value. You can set receipt_date to the date and time in the past when the receipt was created in another system. This value is used in Loyverse back-office reports. |
| `total_discounts[]` | body | `array<object>` | no | The list of all discounts applied in the receipt. Discounts can be applied in two scopes, RECEIPT or LINE_ITEM. For discount with LINE_ITEM level you must reference to corresponding discount in every line item where this discount is applied. For discounts with RECEIPT level, line_discount for every line item will be generated automatically. |
| `note` | body | `string` | no | The receipt's note |
| `line_items[]` | body | `array<object>` | no | The line items included in the receipt |
| `payments[]` | body | `array<object>` | no | The list of payments. There is a restriction that only one payment can be applied to receipt when using POST request. |
