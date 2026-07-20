# Update Task Status with DoneDone

Updates an existing task status in DoneDone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks/:task_id/status`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Update Task Status](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `task_id` | path | `number` | yes | DoneDone task ID. |
| `statusID` | body | `number` | yes | Task status ID. |
