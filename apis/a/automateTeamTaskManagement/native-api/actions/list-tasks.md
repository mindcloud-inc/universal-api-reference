# List Tasks with Automate Team - Task Management

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/t_all_tasks`
- **Base URL:** `https://api.automatebusiness.com`
- **Official documentation:** [List Tasks](https://developers.onautomate.com/task)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `string` | yes | PostgREST filter for the workspace id, for example eq.33371. |
| `task_id` | query | `string` | no | Optional PostgREST filter for a task id, for example eq.12345. |
| `title` | query | `string` | no | Optional PostgREST filter for task titles, for example ilike.*follow-up*. |
| `status` | query | `string` | no | Optional PostgREST filter for status, for example eq.Pending. |
| `priority` | query | `string` | no | Optional PostgREST filter for priority, for example eq.High. |
