# Assign Bib and Chip Numbers with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/assign-bib-chip`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Assign Bib and Chip Numbers](https://runsignup.com/API/race/:race_id/assign-bib-chip/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
| `request` | body | `string` | yes | — |
