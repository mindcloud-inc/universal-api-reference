# Get Race Participant Counts with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/participant-counts`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Get Race Participant Counts](https://runsignup.com/API/race/:race_id/participant-counts/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | ID of event or list of event IDs separated by commas. |
