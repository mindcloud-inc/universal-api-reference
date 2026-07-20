# Get Race with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Get Race](https://runsignup.com/API/race/:race_id/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `future_events_only` | query | `string` | no | Only outputs events that occur in the future. |
| `most_recent_events_only` | query | `string` | no | Only outputs most recent events for the race. |
| `race_event_days_id` | query | `number` | no | Get events by race_event_days_id |
| `race_headings` | query | `string` | no | Include race headings in the output. |
| `race_links` | query | `string` | no | Include race links in the output. |
| `include_waiver` | query | `string` | no | Should waiver be included? |
| `include_multiple_waivers` | query | `string` | no | Should multiple waivers be included? |
| `include_participant_caps` | query | `string` | no | Should participant caps be included? |
| `include_age_based_pricing` | query | `string` | no | Should information on age based pricing be included? |
| `include_giveaway_details` | query | `string` | no | Should give-away (e.g. T-shirt) details be included?  This will include options, such as sizes. |
| `include_questions` | query | `string` | no | Should questions be included? |
| `include_addons` | query | `string` | no | Should registration add-ons be included? |
| `include_membership_settings` | query | `string` | no | Should membership settings be included? |
| `include_corral_settings` | query | `string` | no | Should corral settings be included? |
| `include_donation_settings` | query | `string` | no | Should donations settings be included? |
| `include_extra_date_info` | query | `string` | no | Should extra information about cancellations and postponements be included? |
| `supports_question_application_types` | query | `string` | no | Does your integration support question application types? |
