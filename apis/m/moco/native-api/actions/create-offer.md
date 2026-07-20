# Create Offer with Moco

## Endpoint

- **Method:** `POST`
- **Path:** `/offers`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Create Offer](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#post-offers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `change_address` | body | `string` | no |
| `company_id` | body | `string` | no |
| `contact_id` | body | `string` | no |
| `currency` | body | `string` | no |
| `custom_properties` | body | `string` | no |
| `date` | body | `string` | no |
| `deal_id` | body | `string` | no |
| `discount` | body | `string` | no |
| `due_date` | body | `string` | no |
| `footer` | body | `string` | no |
| `internal_contact_id` | body | `string` | no |
| `items[]` | body | `array<object>` | no |
| `print_detail_columns` | body | `string` | no |
| `project_id` | body | `string` | no |
| `recipient_address` | body | `string` | no |
| `salutation` | body | `string` | no |
| `tags` | body | `string` | no |
| `tax` | body | `string` | no |
| `title` | body | `string` | no |
