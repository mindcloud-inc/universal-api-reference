# Get Channel Files Folder with Microsoft Teams

Retrieves a channel's files folder from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/filesFolder`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Channel Files Folder](https://learn.microsoft.com/en-us/graph/api/channel-get-filesfolder?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
