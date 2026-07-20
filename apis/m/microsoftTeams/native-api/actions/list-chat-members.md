# List Chat Members with Microsoft Teams

Retrieves chat members from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/chats/:chatId/members`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Chat Members](https://learn.microsoft.com/en-us/graph/api/chat-list-members?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Microsoft Graph chat ID. |
