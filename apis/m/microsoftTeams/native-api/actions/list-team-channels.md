# List Team Channels with Microsoft Teams

Retrieves team channels from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/channels`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Team Channels](https://learn.microsoft.com/en-us/graph/api/channel-list?view=graph-rest-1.0)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
