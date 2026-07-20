# Add or Edit Race Participants with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/participants`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Add or Edit Race Participants](https://runsignup.com/API/race/:race_id/participants/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
| `restrict_potential_dup` | body | `string` | yes | — |
| `clear_null_corrals` | body | `string` | no | — |
| `request` | body | `string` | yes | — |
