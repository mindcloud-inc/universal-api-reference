# List Channel Messages with Microsoft Teams

Retrieves channel messages from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Channel Messages](https://learn.microsoft.com/en-us/graph/api/channel-list-messages?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
