# List Timing Data with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/results/get-timing-data`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Timing Data](https://runsignup.com/API/race/:race_id/results/get-timing-data/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
