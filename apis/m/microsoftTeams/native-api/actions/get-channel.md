# Get Channel with Microsoft Teams

Retrieves a channel from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Channel](https://learn.microsoft.com/en-us/graph/api/channel-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
