# Update Deal with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/deals/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Deal](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#put-dealsid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `closed_on` | body | `string` | no |
| `company_id` | body | `string` | no |
| `currency` | body | `string` | no |
| `deal_category_id` | body | `string` | no |
| `id` | path | `number` | yes |
| `info` | body | `string` | no |
| `money` | body | `string` | no |
| `name` | body | `string` | no |
| `person_id` | body | `string` | no |
| `reminder_date` | body | `string` | no |
| `service_period_from` | body | `string` | no |
| `service_period_to` | body | `string` | no |
| `status` | body | `string` | no |
| `tags` | body | `string` | no |
| `user_id` | body | `string` | no |
