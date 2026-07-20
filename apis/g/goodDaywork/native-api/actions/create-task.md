# Create Task with GoodDay.work

Creates a new task in GoodDay.work.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Create Task](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `string` | yes | Task project ID. |
| `title` | body | `string` | yes | Task title. |
| `fromUserId` | body | `string` | yes | User ID creating the task. |
| `toUserId` | body | `string` | no | Assigned or action-required user ID. |
| `estimate` | body | `number` | no | Task estimate in minutes. |
