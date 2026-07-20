# Reply To Channel Message with Microsoft Teams

Creates a reply to a Microsoft Teams channel message.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Reply To Channel Message](https://learn.microsoft.com/en-us/graph/api/chatmessage-post-replies?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
| `messageId` | path | `string` | yes | Microsoft Graph channel message ID. |
| `body.content` | body | `string` | yes | Reply body content. |
