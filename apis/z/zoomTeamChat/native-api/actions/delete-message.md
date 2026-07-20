# Delete Message with Zoom Team Chat

## Endpoint

- **Method:** `DELETE`
- **Path:** `/chat/users/:userId/messages/:messageId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Delete Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/deleteChatMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Unique identifier of the user. |
| `messageId` | path | `string` | yes | Unique identifier of the message. |
| `to_contact` | query | `string` | no | The recipient contact email, member ID, or user ID. |
| `to_channel` | query | `string` | no | The channel ID where the message was sent. |
