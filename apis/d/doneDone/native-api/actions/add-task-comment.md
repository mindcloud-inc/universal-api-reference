# Add Task Comment with DoneDone

Creates a new task comment in DoneDone.

## Endpoint

- **Method:** `POST`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks/:task_id/comment-only`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Add Task Comment](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `task_id` | path | `number` | yes | DoneDone task ID. |
| `message` | body | `string` | yes | Comment body. |
