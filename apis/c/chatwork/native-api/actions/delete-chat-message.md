# Delete Chat Message with Chatwork

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rooms/:room_id/messages/:message_id`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Delete Chat Message](https://developer.chatwork.com/reference/delete-rooms-room_id-messages-message_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `message_id` | path | `string` | yes | Message ID |
