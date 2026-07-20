# React To Chat Message with Zoom Team Chat

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chat/users/:userId/messages/:messageId/emoji_reactions`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [React To Chat Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/reactMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's unique ID. |
| `messageId` | path | `string` | yes | The message's unique ID. |
