# Create Planning Entry with Moco

## Endpoint

- **Method:** `POST`
- **Path:** `/planning_entries`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Create Planning Entry](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#post-planning_entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `comment` | body | `string` | no |
| `deal_id` | body | `string` | no |
| `ends_on` | body | `string` | no |
| `hours_per_day` | body | `string` | no |
| `project_id` | body | `string` | no |
| `starts_on` | body | `string` | no |
| `symbol` | body | `string` | no |
| `tentative` | body | `string` | no |
| `user_id` | body | `string` | no |
