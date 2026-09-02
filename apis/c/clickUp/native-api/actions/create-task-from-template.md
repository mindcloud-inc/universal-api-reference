# Create Task From Template with ClickUp

Creates a task from a ClickUp task template.

## Endpoint

- **Method:** `POST`
- **Path:** `list/:list_id/taskTemplate/:template_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create Task From Template](https://developer.clickup.com/reference/createtaskfromtemplate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list_id` | path | `string` | yes |
| `template_id` | path | `string` | yes |
| `name` | body | `string` | yes |
