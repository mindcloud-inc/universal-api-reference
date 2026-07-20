# List Task Events with Nozbe Teams

Retrieves accessible task events from Nozbe Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/task_events`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Task Events](https://api4.nozbe.com/v1/api#/task_events/getTaskEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Return only events for this task. |
