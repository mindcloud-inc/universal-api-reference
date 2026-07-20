# Update Task with Swipe One

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Update Task](https://docs.swipeone.com/en/articles/10546025-tasks#h_38e3d525a6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Task to update. |
| `name` | body | `string` | no | Updated task name. |
| `assignedTo` | body | `string` | no | Updated task assignee. |
| `dueDate` | body | `date` | no | Updated due date. |
| `reminder` | body | `date` | no | Updated reminder date. |
| `status` | body | `string` | no | Updated task status. |
