# List Channel Tabs with Microsoft Teams

Retrieves channel tabs from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/tabs`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Channel Tabs](https://learn.microsoft.com/en-us/graph/api/channel-list-tabs?view=graph-rest-1.0)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `channelId` | path | `string` | yes | Microsoft Graph channel ID. |
