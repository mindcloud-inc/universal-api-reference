# Unshare Recording from Team with Grain

Unshares a recording from a team in Grain.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/recordings/:recording_id/teams/:team_id`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Unshare Recording from Team](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recording_id` | path | `list<string>` | yes |
| `team_id` | path | `list<string>` | yes |
