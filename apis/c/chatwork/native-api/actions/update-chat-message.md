# Update Chat Message with Chatwork

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:room_id/messages/:message_id`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Update Chat Message](https://developer.chatwork.com/reference/put-rooms-room_id-messages-message_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `message_id` | path | `string` | yes | Message ID |
| `body` | body | `string` | yes | Updated message body Maximum length: 65535. |
