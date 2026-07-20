# Create List From Template with ClickUp

## Endpoint

- **Method:** `POST`
- **Path:** `folder/:folder_id/list_template/:template_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create List From Template](https://developer.clickup.com/reference/createfolderlistfromtemplate)

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
| `template_id` | path | `string` | yes |
