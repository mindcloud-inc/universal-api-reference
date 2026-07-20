# Send Channel Message with Microsoft Teams

Creates a new channel message in Microsoft Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Send Channel Message](https://learn.microsoft.com/en-us/graph/api/channel-post-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
| `body.content` | body | `string` | yes | Message body content. |
