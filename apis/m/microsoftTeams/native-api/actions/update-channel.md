# Update Channel with Microsoft Teams

Updates an existing channel in Microsoft Teams.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Channel](https://learn.microsoft.com/en-us/graph/api/channel-patch?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
| `displayName` | body | `string` | no | Updated channel display name. |
| `description` | body | `string` | no | Updated channel description. |
