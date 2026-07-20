# Get Message with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/messages/:messageId`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Get Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `messageId` | path | `string` | yes | The unique identifier of the message. |
| `to_contact` | query | `string` | no | The recipient contact email, member ID, or user ID. |
| `to_channel` | query | `string` | no | The channel ID where the message was sent. |
| `download_file_formats` | query | `string` | no | Requested file download format. |
