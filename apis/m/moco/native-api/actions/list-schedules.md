# List Schedules with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Schedules](https://everii-group.github.io/mocoapp-api-docs/sections/schedules.html#get-schedules)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `absence_code` | query | `string` | no |
| `custom_properties` | query | `object` | no |
| `from` | query | `date` | no |
| `holiday_request_id` | query | `number` | no |
| `ids` | query | `string` | no |
| `to` | query | `date` | no |
| `updated_after` | query | `date` | no |
| `user_id` | query | `number` | no |
