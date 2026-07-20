# List Team Builds with Codemagic

Retrieves builds for a specific Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id/builds`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Team Builds](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3TeamsTeamIdBuildsListTeamBuilds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
| `app_id` | query | `string` | no | Optional application ID filter for team builds. |
| `workflow_id` | query | `string` | no | Optional workflow ID filter for team builds. |
| `status` | query | `string` | no | Optional build status filter. |
| `branch` | query | `string` | no | Optional branch filter. |
| `tag` | query | `string` | no | Optional tag filter. |
| `label` | query | `string` | no | Optional build label filter. |
| `cursor` | query | `string` | no | Optional next-page cursor for team builds. |
