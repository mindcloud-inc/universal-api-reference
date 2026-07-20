# List Race Corrals with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/corrals`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Corrals](https://runsignup.com/API/race/:race_id/corrals/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `race_event_days_id` | query | `number` | yes | Race event days ID.  This ID groups together events, typically by year.  This ID is returned with the event information in the APIs to get races or a single race. |
