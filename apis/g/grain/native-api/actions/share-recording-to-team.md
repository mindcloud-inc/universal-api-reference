# Share Recording to Team with Grain

Shares a recording with a team in Grain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/recordings/:recording_id/teams/:team_id`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Share Recording to Team](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `team_id` | path | `list<string>` | yes |
