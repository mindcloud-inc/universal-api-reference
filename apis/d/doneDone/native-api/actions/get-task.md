# Get Task with DoneDone

Retrieves a task from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks/:task_id`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Get Task](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `task_id` | path | `number` | yes | DoneDone task ID. |
