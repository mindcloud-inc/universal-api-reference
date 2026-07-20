# Update Entry with Clockodo

Updates a time entry in your Clockodo account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entries/:id`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Update Entry](https://www.clockodo.com/en/api/entries/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billable` | body | `number` | no |
| `customers_id` | body | `string` | no |
| `duration` | body | `number` | no |
| `hourly_rate` | body | `number` | no |
| `lumpsum` | body | `number` | no |
| `lumpsum_services_amount` | body | `number` | no |
| `lumpsum_services_id` | body | `string` | no |
| `projects_id` | body | `string` | no |
| `services_id` | body | `string` | no |
| `text` | body | `string` | no |
| `time_since` | body | `string` | no |
| `time_until` | body | `string` | no |
| `users_id` | body | `string` | no |
