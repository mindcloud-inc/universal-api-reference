# Update Activity with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/activities/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Activity](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#put-activitiesid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billable` | body | `string` | no |
| `date` | body | `string` | no |
| `description` | body | `string` | no |
| `id` | path | `number` | yes |
| `project_id` | body | `string` | no |
| `remote_id` | body | `string` | no |
| `remote_service` | body | `string` | no |
| `remote_url` | body | `string` | no |
| `seconds` | body | `string` | no |
| `tag` | body | `string` | no |
| `task_id` | body | `string` | no |
