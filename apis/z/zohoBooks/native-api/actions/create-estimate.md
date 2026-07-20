# Create Estimate with Zoho Books

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Create Estimate](https://www.zoho.com/books/api/v3/estimates/#create-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list` | yes | — |
| `send` | query | `boolean` | no | — |
| `ignore_auto_number_generation` | query | `boolean` | no | — |
| `customer_id` | body | `list` | yes | — |
| `estimate_number` | body | `string` | no | — |
| `reference_number` | body | `string` | no | — |
| `date` | body | `date` | no | — |
| `expiry_date` | body | `date` | no | — |
| `discount` | body | `string` | no | — |
| `is_discount_before_tax` | body | `boolean` | no | — |
| `discount_type` | body | `list` | no | Accepted values: `0`, `1`. |
| `is_inclusive_tax` | body | `boolean` | no | — |
| `notes` | body | `string` | no | — |
| `terms` | body | `string` | no | — |
| `shipping_charge` | body | `number` | no | — |
| `adjustment` | body | `number` | no | — |
| `adjustment_description` | body | `string` | no | — |
| `location_id` | body | `string` | no | — |
| `project_id` | body | `string` | no | — |
| `accept_retainer` | body | `boolean` | no | — |
| `retainer_percentage` | body | `number` | no | — |
| `line_items[]` | body | `array<object>` | yes | — |
| `line_items[].item_id` | body | `list` | no | — |
| `line_items[].name` | body | `string` | no | — |
| `line_items[].description` | body | `string` | no | — |
| `line_items[].rate` | body | `number` | no | — |
| `line_items[].quantity` | body | `number` | no | — |
| `line_items[].discount_amount` | body | `number` | no | — |
| `line_items[].discount` | body | `string` | no | — |
| `line_items[].location_id` | body | `string` | no | — |
