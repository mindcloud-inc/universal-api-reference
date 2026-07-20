# List Races with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/races`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Races](https://runsignup.com/API/races/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aflt_token` | query | `string` | no | If set, this affiliate token will be appended to race URLs. |
| `events` | query | `string` | no | Includes race events in the output. |
| `race_headings` | query | `string` | no | Include race headings in the output. |
| `race_links` | query | `string` | no | Include race links in the output. |
| `include_waiver` | query | `string` | no | Should waiver be included? |
| `include_multiple_waivers` | query | `string` | no | Should multiple waivers be included? |
| `include_event_days` | query | `string` | no | Should information on events days (e.g. each race year) be included? |
| `include_extra_date_info` | query | `string` | no | Should extra information about cancellations and postponements be included? |
| `include_giveaway_details` | query | `string` | no | Should detailed giveaway information be included? |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `sort` | query | `string` | no | Sort by "name", "date", or "end_date" in ascending ("ASC") or descending ("DESC") order. |
| `name` | query | `string` | no | Search by race name. |
| `start_date` | query | `string` | no | Searches for races that occur on or after a given date. |
| `end_date` | query | `string` | no | Searches for races that occur on or before a given date. |
| `created_since` | query | `string` | no | Searches for races that were created on or after a given date. |
| `created_on_or_before` | query | `string` | no | Searches for races that were created on or before a given date. |
| `modified_since` | query | `string` | no | Searches for races that were modified on or after a given date. |
| `modified_on_or_before` | query | `string` | no | Searches for races that were modified on or before a given date. |
| `only_partner_races` | query | `string` | no | Only get races linked to the partner using the API. |
| `search_start_date_only` | query | `string` | no | Only search race races based on start date, not end date. |
| `only_races_with_results` | query | `string` | no | Only get races that have results. |
| `city` | query | `string` | no | Search by city. |
| `state` | query | `string` | no | Search by state. |
| `country` | query | `string` | no | Search by country. |
| `event_type` | query | `string` | no | Get races by event type. |
| `min_distance` | query | `number` | no | Minimum race distance to get. |
| `max_distance` | query | `number` | no | Maximum race distance to get. |
| `distance_units` | query | `string` | no | Units to use with distance. |
| `zipcode` | query | `string` | no | Searches for races within radius(required) miles from zipcode. US Only. |
| `radius` | query | `number` | no | Searches for races within radius miles from zipcode(required). |
