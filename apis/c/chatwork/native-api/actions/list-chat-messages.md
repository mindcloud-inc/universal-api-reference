# List Chat Messages with Chatwork

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room_id/messages`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [List Chat Messages](https://developer.chatwork.com/reference/get-rooms-room_id-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `force` | query | `list<number>` | no | Whether to force retrieval of the latest messages Accepted values: `0`, `1`. |
