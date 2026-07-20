# Get Task History with DoneDone

Retrieves task history from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/internal-projects/:internal_project_id/tasks/:task_id/history`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [Get Task History](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
| `task_id` | path | `number` | yes | DoneDone task ID. |
| `sort` | query | `string` | no | Sort direction for task history. |
