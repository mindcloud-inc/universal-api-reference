# List Race Group and Team Types with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/teams/team-types`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Group and Team Types](https://runsignup.com/API/race/:race_id/teams/team-types/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | ID of event or list of event IDs separated by commas. |
