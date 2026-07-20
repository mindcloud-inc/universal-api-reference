# Add Task Comment with Planfix

Creates a new task comment in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:id/comments/`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Add Task Comment](https://help.planfix.com/restapidocs/#/Task/post-task-add-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task identifier to comment on. |
| `description` | body | `string` | yes | Comment body. |
| `silent` | query | `boolean` | no | Skip notifications while adding the comment. |
