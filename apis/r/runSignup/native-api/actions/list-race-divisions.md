# List Race Divisions with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/divisions/divisions`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Divisions](https://runsignup.com/API/race/:race_id/divisions/divisions/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
