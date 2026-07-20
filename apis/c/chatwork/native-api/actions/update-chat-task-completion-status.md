# Update Chat Task Completion Status with Chatwork

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:room_id/tasks/:task_id/status`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Update Chat Task Completion Status](https://developer.chatwork.com/reference/put-rooms-room_id-tasks-task_id-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `task_id` | path | `number` | yes | Task ID. |
| `body` | body | `list<string>` | yes | Task status value. Use open to reopen a task or done to complete it. Accepted values: `done`, `open`. |
