# List Chat Installed Apps with Microsoft Teams

Retrieves installed apps for a Microsoft Teams chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/chats/:chatId/installedApps`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Chat Installed Apps](https://learn.microsoft.com/en-us/graph/api/chat-list-installedapps?view=graph-rest-1.0&tabs=http)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Microsoft Teams chat ID. |
