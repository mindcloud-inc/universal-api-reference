# Update Task with Frameshift

Updates an existing task in Frameshift.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:project_id/tasks/:task_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Update Task](https://mosaic.frameshift.io/api/#api-Tasks-EditTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |
| `completed` | body | `boolean` | no |
| `message` | body | `string` | no |
