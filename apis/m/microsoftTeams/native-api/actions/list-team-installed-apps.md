# List Team Installed Apps with Microsoft Teams

Retrieves installed apps for a Microsoft Teams team.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/installedApps`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Team Installed Apps](https://learn.microsoft.com/en-us/graph/api/team-list-installedapps?view=graph-rest-1.0)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
