# List Team Members with Microsoft Teams

Retrieves team members from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/members`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Team Members](https://learn.microsoft.com/en-us/graph/api/team-list-members?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
