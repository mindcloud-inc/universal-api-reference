# List Tasks with Nozbe Teams

Retrieves accessible tasks from Nozbe Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Tasks](https://api4.nozbe.com/v1/api#/tasks/getTasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Return only tasks from this project. |
