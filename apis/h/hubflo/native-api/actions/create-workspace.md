# Create Workspace with Hubflo

Creates a new workspace in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Workspace](https://hubflo.readme.io/reference/post_api-v2-workspaces)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `subtitle` | body | `string` | no |
| `welcome_message` | body | `string` | no |
| `chat_room_id` | body | `string` | no |
| `new_chat_room` | body | `boolean` | no |
| `user_ids` | body | `list<string>` | no |
| `project_id` | body | `string` | no |
| `template_id` | body | `string` | no |
| `tags` | body | `list<string>` | no |
