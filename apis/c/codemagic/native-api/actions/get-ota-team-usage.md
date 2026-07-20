# Get OTA Team Usage with Codemagic

Retrieves over-the-air update usage for a Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/over-the-air-updates/:team_id/usage`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get OTA Team Usage](https://codemagic.io/api/v3/schema#tag/Over-the-air%20Updates/operation/ApiV3OverTheAirUpdatesTeamIdUsageGetUsage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
| `period_from` | query | `date` | no | Optional usage-period start timestamp or date. |
| `period_to` | query | `date` | no | Optional usage-period end timestamp or date. |
