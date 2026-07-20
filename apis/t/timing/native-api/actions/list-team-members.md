# List Team Members with Timing

Retrieves active team members from Timing.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team_id/members`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [List Team Members](https://web.timingapp.com/docs/#teams-GETapi-v1-teams--team_id--members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | The Timing team ID whose members should be listed. |
