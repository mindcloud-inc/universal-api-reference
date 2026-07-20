# List Task Summaries with Timely

Retrieves task summaries from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/forecasts/{resource}/summary`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Task Summaries](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `resource` | path | `string` | yes | Resource type to group summaries by |
| `since` | query | `date` | no | Filter tasks from this date |
| `until` | query | `date` | no | Filter tasks up to this date |
| `completed` | query | `string` | no | Filter by completion status |
| `user_ids` | query | `string` | no | Comma-separated user IDs to filter by |
| `project_ids` | query | `string` | no | Comma-separated project IDs to filter by |
| `forecast_ids` | query | `string` | no | Comma-separated task IDs to filter by |
