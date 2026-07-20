# Update Team with HeadshotPro

Updates an existing team in HeadshotPro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organization/teams/:teamId`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Update Team](https://www.headshotpro.com/api/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team to update. |
| `name` | body | `string` | yes | New unique name for the team. |
