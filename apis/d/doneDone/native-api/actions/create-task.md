# Create Task with DoneDone

Creates a new task in DoneDone.

## Endpoint

- **Method:** `POST`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Create Task](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `title` | body | `string` | yes | Task title. |
| `description` | body | `string` | no | Task description. |
| `statusID` | body | `number` | no | Task status ID. |
| `priorityID` | body | `number` | no | Task priority ID. |
