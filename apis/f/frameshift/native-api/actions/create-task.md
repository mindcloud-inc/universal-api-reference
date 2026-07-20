# Create Task with Frameshift

Creates a new task in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/tasks`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Task](https://mosaic.frameshift.io/api/#api-Tasks-CreateTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `type` | body | `string` | yes |
| `message` | body | `string` | no |
| `attribute_id` | body | `number` | no |
| `variant_set_id` | body | `number` | no |
