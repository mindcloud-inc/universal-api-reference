# Search Tasks with Runrun.it

Finds tasks in Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Search Tasks](https://runrun.it/api/documentation#tasks-query-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | IDs of tasks, separated by comma |
| `user_id` | query | `string` | no | ID of user who created the task |
| `follower_id` | query | `string` | no | ID of user following the task |
| `project_id` | query | `number` | no | ID of the project the task belongs to |
| `is_closed` | query | `boolean` | no | True if the task is delivered |
| `is_working_on` | query | `boolean` | no | True if any assignee is working on task |
| `sort` | query | `string` | no | Sort strategy. |
| `sort_dir` | query | `string` | no | Sort direction. Must be asc or desc |
| `bypass_status_default` | query | `boolean` | no | Set as true to bypass the default value of is_closed param |
