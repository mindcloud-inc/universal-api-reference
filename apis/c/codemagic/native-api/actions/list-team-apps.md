# List Team Apps with Codemagic

Retrieves apps for a specific Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id/apps`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Team Apps](https://codemagic.io/api/v3/schema#tag/Applications/operation/ApiV3TeamsTeamIdAppsListTeamApps)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
| `id` | query | `string` | no | Optional app ID filter documented by Codemagic for team apps. |
