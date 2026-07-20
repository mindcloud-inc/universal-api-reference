# Update Estimate with Zoho Books

## Endpoint

- **Method:** `PUT`
- **Path:** `/estimates/:estimate_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Update Estimate](https://www.zoho.com/books/api/v3/estimates/#update-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `list` | yes | — |
| `organization_id` | query | `list` | yes | — |
| `ignore_auto_number_generation` | query | `boolean` | no | — |
| `customer_id` | body | `list` | yes | — |
| `estimate_number` | body | `string` | no | Unique identifier for the estimate when overriding auto numbering. |
| `reference_number` | body | `string` | no | — |
| `date` | body | `date` | no | Date the estimate is created in YYYY-MM-DD format. |
| `expiry_date` | body | `date` | no | Date when the estimate expires in YYYY-MM-DD format. |
| `notes` | body | `string` | no | — |
| `line_items[]` | body | `array<object>` | no | — |
| `line_items[].line_item_id` | body | `string` | no | — |
| `line_items[].item_id` | body | `list` | no | — |
| `line_items[].description` | body | `string` | no | — |
| `line_items[].rate` | body | `number` | no | Unit price for the line item. |
| `line_items[].quantity` | body | `number` | no | Number of units for the line item. |
