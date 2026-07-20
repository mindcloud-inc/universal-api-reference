# Edit Event Result Set with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/results/edit-result-set`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Edit Event Result Set](https://runsignup.com/API/race/:race_id/results/edit-result-set/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
| `individual_result_set_id` | query | `number` | yes | ID of result set. |
| `request` | body | `string` | yes | — |
