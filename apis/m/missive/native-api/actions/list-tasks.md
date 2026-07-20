# List Tasks with Missive

Retrieves tasks from your Missive workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Tasks](https://missiveapp.com/docs/developers/rest-api/endpoints#list-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | no | Filter by organization ID. |
| `team` | query | `string` | no | Filter by team ID. |
| `assignee` | query | `string` | no | Filter by assignee user ID. |
| `state` | query | `list` | no | Filter by task state. Accepted values: `closed`, `in_progress`, `todo`. |
| `type` | query | `list` | no | Filter by task type. Accepted values: `all`, `conversation`, `task`. |
| `conversation` | query | `string` | no | Filter by parent conversation ID. |
| `due_at_gteq` | query | `date` | no | Filter tasks with due_at greater than or equal to this Unix timestamp. |
| `due_at_lteq` | query | `date` | no | Filter tasks with due_at less than or equal to this Unix timestamp. |
| `until` | query | `date` | no | Unix timestamp for pagination. Returns tasks with last_activity_at before this value. |
