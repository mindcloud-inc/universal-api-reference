# List User's Chat Sessions with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/sessions`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List User's Chat Sessions](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatSessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID of the sessions being queried. |
| `type` | query | `string` | no | The session type to query. |
| `search_star` | query | `boolean` | no | Search only starred chats. |
| `from` | query | `string` | no | The start timestamp in ISO-8601 format. |
| `to` | query | `string` | no | The end timestamp in ISO-8601 format. |
