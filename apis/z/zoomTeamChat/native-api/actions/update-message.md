# Update Message with Zoom Team Chat

## Endpoint

- **Method:** `PUT`
- **Path:** `/chat/users/:userId/messages/:messageId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Update Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/editMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `messageId` | path | `string` | yes | The unique identifier of the message. |
| `to_contact` | query | `string` | no | The contact email address where the message was sent. |
| `to_channel` | query | `string` | no | The channel ID where the message was sent. |
| `message` | body | `string` | no | The updated message content. |
