# Mark Message Read Or Unread with Zoom Team Chat

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chat/users/:userId/messages/:messageId/status`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Mark Message Read Or Unread](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/markMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `messageId` | path | `string` | yes | The unique identifier of the message. |
