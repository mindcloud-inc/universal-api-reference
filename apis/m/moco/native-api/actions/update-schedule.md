# Update Schedule with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/schedules/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Schedule](https://everii-group.github.io/mocoapp-api-docs/sections/schedules.html#put-schedulesid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `absence_code` | body | `string` | no |
| `am` | body | `string` | no |
| `comment` | body | `string` | no |
| `date` | body | `string` | no |
| `id` | path | `number` | yes |
| `overwrite` | body | `string` | no |
| `pm` | body | `string` | no |
| `symbol` | body | `string` | no |
| `user_id` | body | `string` | no |
