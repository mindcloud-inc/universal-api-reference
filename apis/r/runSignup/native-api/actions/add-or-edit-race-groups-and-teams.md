# Add or Edit Race Groups and Teams with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/teams`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Add or Edit Race Groups and Teams](https://runsignup.com/API/race/:race_id/teams/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | Id of event or list of event ids separated by commas. |
| `request` | body | `string` | yes | — |
