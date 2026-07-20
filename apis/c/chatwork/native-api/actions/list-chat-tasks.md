# List Chat Tasks with Chatwork

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room_id/tasks`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [List Chat Tasks](https://developer.chatwork.com/reference/get-rooms-room_id-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `account_id` | query | `number` | no | Account ID. |
| `assigned_by_account_id` | query | `number` | no | Account ID of the user who assigned the task. |
| `status` | query | `list<string>` | no | Completion status of the task. Accepted values: `done`, `open`. |
