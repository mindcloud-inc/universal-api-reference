# Update Task Priority with DoneDone

Updates an existing task priority in DoneDone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks/:task_id/priority`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Update Task Priority](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `task_id` | path | `number` | yes | DoneDone task ID. |
| `priorityID` | body | `number` | yes | Task priority ID. |
