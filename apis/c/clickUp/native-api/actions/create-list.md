# Create List with ClickUp

Creates a new List in a ClickUp Folder.

## Endpoint

- **Method:** `POST`
- **Path:** `folder/:folder_id/list`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create List](https://developer.clickup.com/reference/createlist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignee` | body | `number` | no |
| `name` | body | `string` | yes |
| `content` | body | `string` | no |
| `due_date` | body | `date` | no |
| `due_date_time` | body | `boolean` | no |
| `folder_id` | path | `string` | yes |
| `markdown_content` | body | `string` | no |
| `priority` | body | `list` | no |
| `status` | body | `string` | no |
