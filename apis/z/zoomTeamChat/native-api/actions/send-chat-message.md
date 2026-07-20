# Send Chat Message with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/users/:userId/messages`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Send Chat Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/sendaChatMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `message` | body | `string` | yes | The message content. |
| `to_contact` | body | `string` | no | The contact email address for a 1:1 message. |
| `to_channel` | body | `string` | no | The channel ID for a channel message. |
