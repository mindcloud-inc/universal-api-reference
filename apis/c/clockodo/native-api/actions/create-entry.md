# Create Entry with Clockodo

Creates a time entry in your Clockodo account.

## Endpoint

- **Method:** `POST`
- **Path:** `/entries`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Create Entry](https://www.clockodo.com/en/api/entries/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billable` | body | `number` | yes |
| `customers_id` | body | `string` | yes |
| `duration` | body | `number` | no |
| `hourly_rate` | body | `number` | no |
| `projects_id` | body | `string` | no |
| `services_id` | body | `string` | yes |
| `text` | body | `string` | no |
| `time_since` | body | `string` | yes |
| `time_until` | body | `string` | yes |
| `users_id` | body | `string` | no |
