# Update Chat with Chatwork

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:room_id`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [Update Chat](https://developer.chatwork.com/reference/put-rooms-room_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Room ID |
| `name` | body | `string` | no | Chat name Maximum length: 255. |
| `description` | body | `string` | no | Chat description |
| `icon_preset` | body | `list<string>` | no | Chat icon type Accepted values: `beer`, `business`, `check`, `document`, `event`, `group`, `heart`, `idea`, `magcup`, `meeting`, `music`, `project`, `security`, `sports`, `star`, `study`, `travel`. |
