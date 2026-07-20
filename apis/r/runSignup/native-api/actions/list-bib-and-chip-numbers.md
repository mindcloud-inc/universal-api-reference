# List Bib and Chip Numbers with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/get-bib-chip`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Bib and Chip Numbers](https://runsignup.com/API/race/:race_id/get-bib-chip/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
