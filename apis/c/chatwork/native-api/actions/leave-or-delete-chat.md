# Leave or Delete Chat with Chatwork

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rooms/:room_id`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Leave or Delete Chat](https://developer.chatwork.com/reference/delete-rooms-room_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `action_type` | body | `list<string>` | yes | Whether to leave or delete the room Accepted values: `delete`, `leave`. |
