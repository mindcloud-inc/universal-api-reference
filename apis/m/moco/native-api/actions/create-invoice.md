# Create Invoice with Moco

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Create Invoice](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#post-invoices)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cash_discount` | body | `string` | no |
| `cash_discount_days` | body | `string` | no |
| `change_address` | body | `string` | no |
| `currency` | body | `string` | no |
| `custom_properties` | body | `string` | no |
| `customer_id` | body | `string` | no |
| `date` | body | `string` | no |
| `discount` | body | `string` | no |
| `due_date` | body | `string` | no |
| `footer` | body | `string` | no |
| `internal_contact_id` | body | `string` | no |
| `items[]` | body | `array<object>` | no |
| `print_detail_columns` | body | `string` | no |
| `project_id` | body | `string` | no |
| `recipient_address` | body | `string` | no |
| `salutation` | body | `string` | no |
| `service_period_from` | body | `string` | no |
| `service_period_to` | body | `string` | no |
| `status` | body | `string` | no |
| `tags` | body | `string` | no |
| `tax` | body | `string` | no |
| `title` | body | `string` | no |
