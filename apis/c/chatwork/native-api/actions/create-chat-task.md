# Create Chat Task with Chatwork

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room_id/tasks`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Create Chat Task](https://developer.chatwork.com/reference/post-rooms-room_id-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `body` | body | `string` | yes | Task content. Maximum length: 65535. |
| `to_ids` | body | `string` | yes | Comma-separated account IDs assigned to the task. Send multiple values as a string separated by `,`. |
| `limit` | body | `number` | no | Unix timestamp in seconds for the task deadline. |
| `limit_type` | body | `list<string>` | no | Deadline interpretation. Accepted values: `date`, `none`, `time`. |
