# List Race Groups and Teams with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/teams`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Groups and Teams](https://runsignup.com/API/race/:race_id/teams/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | Id of event or list of event ids separated by commas. |
| `modified_since` | query | `string` | no | Get teams modified on or after a given time.  If set, groups are returned in order of last modified date.  Otherwise, by group name. |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `include_group_sizes` | query | `string` | no | Include group sizes |
