# List Removed Race Participants with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/removed-participants`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Removed Race Participants](https://runsignup.com/API/race/:race_id/removed-participants/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | ID of event or list of event IDs separated by commas. |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `sort` | query | `string` | no | Sort by "registration_id", "registration_date" or "last_modified" in ascending ("ASC") or descending ("DESC") order. |
| `after_registration_id` | query | `number` | no | Get registrations after the given registration ID. |
| `modified_after_timestamp` | query | `string` | no | Get registrations modified on or after a given time. |
| `condensed_format` | query | `string` | no | Use the condensed format, which only includes IDs and the reason for removal from the race. |
| `supports_nb` | query | `string` | no | Does integration support non-binary X gender? |
