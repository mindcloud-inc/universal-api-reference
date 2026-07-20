# Create Task with Microsoft 365 Planner

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/planner/tasks`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Task](https://learn.microsoft.com/en-us/graph/api/planner-post-tasks?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the new Planner task. |
| `planId` | body | `string` | yes | Planner plan ID where the task should be created. |
| `bucketId` | body | `string` | no | Planner bucket ID for the new task. |
| `dueDateTime` | body | `string` | no | Optional task due date/time in ISO 8601 format. |
| `startDateTime` | body | `string` | no | Optional task start date/time in ISO 8601 format. |
| `percentComplete` | body | `number` | no | Optional completion percentage from 0 to 100. |
| `priority` | body | `number` | no | Optional Planner priority value from 0 to 10. |
