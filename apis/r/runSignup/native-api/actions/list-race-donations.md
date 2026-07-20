# List Race Donations with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/donations/list`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Donations](https://runsignup.com/API/race/:race_id/donations/list/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `since_ts` | query | `number` | no | Get donations on or after the provided timestamp. |
| `until_ts` | query | `number` | no | Get donations on or before the provided timestamp. |
| `supports_nb` | query | `string` | no | Does integration support non-binary X gender? |
| `sort_direction` | query | `string` | no | Sort direction based on donation ID ("ASC" or "DESC"). |
| `before_donation_id` | query | `number` | no | Get donations strictly less than the provided ID. |
| `after_donation_id` | query | `number` | no | Get donations strictly greater than the provided ID. |
| `include_on_behalf_of_labels` | query | `string` | no | Should on behalf of labels be included? |
