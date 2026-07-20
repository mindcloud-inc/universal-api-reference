# List Available Time Slots with Orbit AI (Forms)

## Endpoint

- **Method:** `GET`
- **Path:** `/api/calendar/availability`
- **Base URL:** `https://orbitforms.ai`
- **Official documentation:** [List Available Time Slots](https://docs.orbitforms.ai/developers/api/scheduling#get-available-time-slots)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | query | `string` | yes |
| `team_id` | query | `string` | yes |
| `date` | query | `date` | yes |
