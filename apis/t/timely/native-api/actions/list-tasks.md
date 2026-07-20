# List Tasks with Timely

Retrieves tasks from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/forecasts`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Tasks](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `since` | query | `date` | no | Filter tasks from this date (inclusive) |
| `upto` | query | `date` | no | Filter tasks up to this date (inclusive) |
| `completed` | query | `string` | no | Filter by completion status |
| `user_ids` | query | `string` | no | Comma-separated list of user IDs to filter by |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs, or "active"/"archived" to filter by project status |
| `forecast_ids` | query | `string` | no | Comma-separated list of task IDs to filter by |
| `sort` | query | `string` | no | Field to sort by (default: updated_at) |
| `order` | query | `string` | no | Sort order (default: desc) |
