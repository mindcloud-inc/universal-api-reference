# Mark Message Unread with Chatwork

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:room_id/messages/unread`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Mark Message Unread](https://developer.chatwork.com/reference/put-rooms-room_id-messages-unread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID. |
| `message_id` | body | `string` | yes | Message ID to mark as unread. |
