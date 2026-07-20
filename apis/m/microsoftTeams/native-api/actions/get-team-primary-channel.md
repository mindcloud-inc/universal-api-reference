# Get Team Primary Channel with Microsoft Teams

Retrieves a team's primary channel from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/teams/:teamId/primaryChannel`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Team Primary Channel](https://learn.microsoft.com/en-us/graph/api/team-get-primarychannel?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
