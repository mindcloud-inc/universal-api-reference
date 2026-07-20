# Create Estimate Item with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates/:estimate_id/items`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Create Estimate Item](https://roapp.readme.io/reference/create-estimate-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `number` | yes | Estimate ID |
| `entity_id` | body | `number` | yes | Product or Service ID |
| `assignee_id` | body | `number` | yes | Assigned Employee ID |
| `quantity` | body | `number` | yes | Quantity |
| `price` | body | `number` | yes | Price per unit |
| `cost` | body | `number` | yes | Unit cost |
| `discount` | body | `object` | yes | Item discount object |
| `discount.type` | body | `string` | yes | Discount type. "percentage" — percent, "value" — absolute value. |
| `discount.percentage` | body | `number` | yes | Percentage value |
| `discount.amount` | body | `number` | yes | — |
| `discount.sponsor` | body | `string` | yes | "staff" — Employee wages calculation is based on the amount after discount. This way the company discount decreases the piecework employee wages. "company" — Employee commissions will be calculated from amount before discount. This way the company discount won't affect the employee commissions. |
| `warranty` | body | `object` | yes | Item warranty object |
| `warranty.period` | body | `string` | yes | Warranty period |
| `warranty.periodUnits` | body | `string` | yes | Warranty unit of measure |
| `tax_ids[]` | body | `array<number>` | no | Array of Tax ID |
| `comment` | body | `string` | no | Comment text |
