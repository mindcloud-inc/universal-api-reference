# Update Workspace with Hubflo

Updates an existing workspace in Hubflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:id`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Update Workspace](https://hubflo.readme.io/reference/patch_api-v2-workspaces-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `title` | body | `string` | yes |
| `subtitle` | body | `string` | no |
| `welcome_message` | body | `string` | no |
| `chat_room_id` | body | `string` | no |
| `project_id` | body | `string` | no |
| `tags` | body | `list<string>` | no |
