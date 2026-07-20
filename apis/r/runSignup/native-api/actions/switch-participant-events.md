# Switch Participant Events with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/switch-participant-events`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Switch Participant Events](https://runsignup.com/API/race/:race_id/switch-participant-events/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `transfer_bibs` | body | `string` | no | — |
| `preserve_teams` | body | `string` | no | — |
| `request` | body | `string` | yes | — |
