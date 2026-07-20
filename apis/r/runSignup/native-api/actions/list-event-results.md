# List Event Results with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/results/get-results`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Event Results](https://runsignup.com/API/race/:race_id/results/get-results/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `number` | yes | ID of event. |
| `individual_result_set_id` | query | `number` | no | ID of result set. |
| `include_total_finishers` | query | `string` | no | Indicates whether or not to include total finishers in result set metadata. (Not supported for CSV) |
| `include_split_time_ms` | query | `string` | no | Indicates whether or not to include milliseconds in split times. |
| `modified_after_timestamp` | query | `string` | no | Get results modified after a given timestamp |
| `supports_nb` | query | `string` | no | Does integration support non-binary X gender? |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `first_name` | query | `string` | no | Search for results by first name. |
| `last_name` | query | `string` | no | Search for results by last name. |
| `gender` | query | `string` | no | Search for results by gender. |
| `bib_num` | query | `number` | no | Search for results by bib number. |
| `registration_id` | query | `number` | no | Search for results by registration ID. |
| `min_place` | query | `number` | no | Search for results by minimum finishing place. |
| `max_place` | query | `number` | no | Search for results by maximum finishing place. |
| `min_age` | query | `number` | no | Search for results by minimum age. |
| `max_age` | query | `number` | no | Search for results by maximum age. |
| `state` | query | `string` | no | Search for results by state. |
| `country` | query | `string` | no | Search for results by country. |
