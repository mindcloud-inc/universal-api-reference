# Update Task with Manus

Updates task metadata in Manus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:task_id`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Update Task](https://open.manus.ai/docs/v1/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The ID of the task to update |
| `title` | body | `string` | no | New title for the task |
| `enableShared` | body | `boolean` | no | Make the task publicly accessible |
| `enableVisibleInTaskList` | body | `boolean` | no | Show the task in the Manus web app task list |
