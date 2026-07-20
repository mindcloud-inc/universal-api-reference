# Add Members To Team with HeadshotPro

Adds members to a team in HeadshotPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/teams/:teamId/members`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Add Members To Team](https://www.headshotpro.com/api/team-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team that should receive the members. |
| `emails` | body | `string` | yes | Email addresses of existing organization members to move into the team. Send multiple values as a array. |
