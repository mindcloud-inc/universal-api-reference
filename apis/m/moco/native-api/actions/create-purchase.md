# Create Purchase with Moco

## Endpoint

- **Method:** `POST`
- **Path:** `/purchases`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Create Purchase](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#post-purchases)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | body | `string` | no |
| `currency` | body | `string` | no |
| `custom_property_values` | body | `string` | no |
| `date` | body | `string` | no |
| `due_date` | body | `string` | no |
| `file` | body | `string` | no |
| `iban` | body | `string` | no |
| `info` | body | `string` | no |
| `items[]` | body | `array<object>` | no |
| `payment_method` | body | `string` | no |
| `receipt_identifier` | body | `string` | no |
| `reference` | body | `string` | no |
| `service_period_from` | body | `string` | no |
| `service_period_to` | body | `string` | no |
| `status` | body | `string` | no |
| `tags` | body | `string` | no |
| `title` | body | `string` | no |
| `user_id` | body | `string` | no |
