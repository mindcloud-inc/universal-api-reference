# Update Planning Entry with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/planning_entries/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Planning Entry](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#put-planning_entriesid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `comment` | body | `string` | no |
| `deal_id` | body | `string` | no |
| `ends_on` | body | `string` | no |
| `hours_per_day` | body | `string` | no |
| `id` | path | `number` | yes |
| `project_id` | body | `string` | no |
| `starts_on` | body | `string` | no |
| `symbol` | body | `string` | no |
| `tentative` | body | `string` | no |
| `user_id` | body | `string` | no |
