# Get a team's projects with Asana

Retrieves a team's projects from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:team_gid/projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a team's projects](https://developers.asana.com/reference/getprojectsforteam)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | — |
| `team_gid` | path | `string` | yes | Path parameter: team_gid |
| `limit` | query | `number` | no | — |
| `offset` | query | `string` | no | — |
| `opt_fields[]` | query | `array<string>` | no | — |
