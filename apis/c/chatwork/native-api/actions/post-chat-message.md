# Post Chat Message with Chatwork

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room_id/messages`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Post Chat Message](https://developer.chatwork.com/reference/post-rooms-room_id-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `body` | body | `string` | yes | Message body Maximum length: 65535. |
| `self_unread` | body | `list<number>` | no | Whether to mark the posted message as unread for yourself Accepted values: `0`, `1`. |
