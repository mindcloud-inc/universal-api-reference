# List Corporate Teams with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/corporate-teams`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Corporate Teams](https://runsignup.com/API/race/:race_id/corporate-teams/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `race_event_days_id` | query | `number` | yes | Race event days ID.  This ID groups together events, typically by year.  This ID is returned with the event information in the APIs to get races or a single race. |
| `include_team_sizes` | query | `string` | no | Include team sizes |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
