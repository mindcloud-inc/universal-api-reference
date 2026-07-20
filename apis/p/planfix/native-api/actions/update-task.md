# Update Task with Planfix

Updates an existing task in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Update Task](https://help.planfix.com/restapidocs/#/Task/post-task-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Planfix task identifier. |
| `name` | body | `string` | no | Updated task name. |
| `description` | body | `string` | no | Updated task description. |
| `silent` | query | `boolean` | no | Skip notifications while updating. |
