# List OTA Projects with Codemagic

Retrieves over-the-air update projects for a Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/over-the-air-updates/:team_id/projects`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List OTA Projects](https://codemagic.io/api/v3/schema#tag/Over-the-air%20Updates/operation/ApiV3OverTheAirUpdatesTeamIdProjectsListProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
