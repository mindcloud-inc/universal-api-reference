# Update Order Item with RO App

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/:order_id/items/:item_id`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Order Item](https://roapp.readme.io/reference/update-order-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | Order ID |
| `item_id` | path | `number` | yes | Order Item ID |
| `assignee_id` | body | `number` | no | Assigned Employee ID |
| `quantity` | body | `number` | no | Quantity |
| `price` | body | `number` | no | Price per unit |
| `cost` | body | `number` | no | Unit cost |
| `discount` | body | `object` | no | Item discount object |
| `discount.type` | body | `string` | yes | Discount type. "percentage" — percent, "value" — absolute value. |
| `discount.percentage` | body | `number` | yes | Percentage value |
| `discount.amount` | body | `number` | yes | — |
| `discount.sponsor` | body | `string` | yes | "staff" — Employee wages calculation is based on the amount after discount. This way the company discount decreases the piecework employee wages. "company" — Employee commissions will be calculated from amount before discount. This way the company discount won't affect the employee commissions. |
| `warranty` | body | `object` | no | Item warranty object |
| `warranty.period` | body | `string` | yes | Warranty period |
| `warranty.periodUnits` | body | `string` | yes | Warranty unit of measure |
| `tax_ids[]` | body | `array<number>` | no | Array of Tax ID |
| `comment` | body | `string` | no | Comment text |
