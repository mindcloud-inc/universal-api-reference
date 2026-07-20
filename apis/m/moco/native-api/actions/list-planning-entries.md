# List Planning Entries with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/planning_entries`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Planning Entries](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#get-planning_entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_properties` | query | `object` | no |
| `deal_id` | query | `number` | no |
| `ids` | query | `string` | no |
| `period` | query | `string` | no |
| `project_id` | query | `number` | no |
| `updated_after` | query | `date` | no |
| `user_id` | query | `number` | no |
