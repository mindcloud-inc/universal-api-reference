# Update Project with Pushpad

Updates an existing project in Pushpad.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Update Project](https://pushpad.xyz/docs/rest_api#projects_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `badge_url` | body | `string` | no |
| `icon_url` | body | `string` | no |
| `name` | body | `string` | no |
| `notifications_require_interaction` | body | `boolean` | no |
| `notifications_silent` | body | `boolean` | no |
| `notifications_ttl` | body | `number` | no |
| `project_id` | path | `number` | yes |
| `website` | body | `string` | no |
