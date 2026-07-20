# Create Chat with Microsoft Teams

Creates a new chat in Microsoft Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/chats`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Chat](https://learn.microsoft.com/en-us/graph/api/chat-post?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatType` | body | `string` | yes | Chat type, for example oneOnOne or group. |
| `members[]` | body | `array<object>` | yes | Array of conversation member objects. Include every participant, including the initiating user. Each item should include @odata.type, roles, and user@odata.bind per Microsoft Graph create chat docs. |
| `topic` | body | `string` | no | Topic for group chats. |
