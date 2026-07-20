# Get Team with Codemagic

Retrieves a specific team from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Team](https://codemagic.io/api/v3/schema#tag/Teams/operation/ApiV3TeamsTeamIdGetTeam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
