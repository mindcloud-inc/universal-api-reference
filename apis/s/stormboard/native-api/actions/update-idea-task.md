# Update Idea Task with Stormboard

Updates an idea task in Stormboard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ideas/:idea_id/task`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Update Idea Task](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_to` | body | `string` | no | Stormboard user ID to assign to the task. |
| `date_completed` | body | `string` | no | Task completion date in YYYY-MM-DD format. |
| `date_due` | body | `string` | no | Task due date in YYYY-MM-DD format. |
| `idea_id` | path | `number` | yes | Idea ID from a Stormboard idea record. |
| `notify` | body | `string` | no | Set to 1 to notify the assignee, or 0 to skip the notification. |
