# List Event Result Sets with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/results/get-result-sets`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Event Result Sets](https://runsignup.com/API/race/:race_id/results/get-result-sets/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
| `include_total_finishers` | query | `string` | no | Indicates whether or not to include total finishers in result set metadata. (Not supported for CSV) |
| `include_division_finishers` | query | `string` | no | Indicates whether or not to include division finishers in result set metadata. (Not supported for CSV). Division finishers will only be included if include_total_finishers is also set to T. |
