# Update Invoice with Harvest

Updates an existing invoice in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/invoices/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Invoice](https://help.getharvest.com/api-v2/invoices-api/invoices/invoices/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `client_id` | body | `number` | no |
| `retainer_id` | body | `number` | no |
| `estimate_id` | body | `number` | no |
| `purchase_order` | body | `string` | no |
| `tax` | body | `number` | no |
| `tax2` | body | `number` | no |
| `discount` | body | `number` | no |
| `subject` | body | `string` | no |
| `notes` | body | `string` | no |
| `currency` | body | `string` | no |
| `issue_date` | body | `string` | no |
| `due_date` | body | `string` | no |
| `payment_term` | body | `string` | no |
| `payment_options[]` | body | `array<string>` | no |
| `line_items[].kind` | body | `string` | no |
| `line_items[].description` | body | `string` | no |
| `line_items[].quantity` | body | `number` | no |
| `line_items[].unit_price` | body | `number` | no |
| `line_items[].project_id` | body | `number` | no |
