# List Channel Message Replies with Microsoft Teams

Retrieves replies to a Microsoft Teams channel message.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Channel Message Replies](https://learn.microsoft.com/en-us/graph/api/chatmessage-list-replies?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
| `messageId` | path | `string` | yes | Microsoft Graph channel message ID. |
