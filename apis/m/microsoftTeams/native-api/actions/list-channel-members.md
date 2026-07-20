# List Channel Members with Microsoft Teams

Retrieves channel members from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/members`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Channel Members](https://learn.microsoft.com/en-us/graph/api/channel-list-members?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
