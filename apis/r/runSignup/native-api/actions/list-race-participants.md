# List Race Participants with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/race/:race_id/participants`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Participants](https://runsignup.com/API/race/:race_id/participants/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `event_id` | query | `string` | yes | ID of event or list of event IDs separated by commas. |
| `page` | query | `number` | no | Page number to get. |
| `results_per_page` | query | `number` | no | Number of results per page. |
| `sort` | query | `string` | no | Sort by "registration_id", "registration_date", "age", "name", "first_name", "last_name", "bib_num", "chip_num", "gender" in ascending ("ASC") or descending ("DESC") order. |
| `after_registration_id` | query | `number` | no | Get registrations after the given registration ID |
| `before_registration_id` | query | `number` | no | Get registrations before the given registration ID |
| `modified_after_timestamp` | query | `string` | no | Get registrations modified on or after a given time |
| `registered_after_timestamp` | query | `string` | no | Get registrations registered on or after a given time |
| `registered_before_timestamp` | query | `string` | no | Get registrations registered on or before a given time |
| `include_counties` | query | `string` | no | Should the US counties (NOT COUNTRY) be included. |
| `include_template_participant` | query | `string` | no | Should a template participant be included. Registration ID will be -1. |
| `include_user_anonymous_flag` | query | `string` | no | Should the is_anonymous flag be included on users? |
| `include_questions` | query | `string` | no | Should question responses be included. Ignored for CSV response type. |
| `include_corrals` | query | `string` | no | Should corrals be included. |
| `include_est_finish` | query | `string` | no | Should estimated finish times be included. |
| `include_corp_teams` | query | `string` | no | Should corporate teams be included. |
| `include_registration_addons` | query | `string` | no | Should registration add-ons be included. Ignored for CSV response type. |
| `include_memberships` | query | `string` | no | Should registration memberships be included. Ignored for CSV response type. |
| `include_coupon_details` | query | `string` | no | Should coupon details be included. |
| `include_registration_notes` | query | `string` | no | Should registration notes be included. |
| `include_checkin_data` | query | `string` | no | Should checkin data be included. |
| `include_waiver_info` | query | `string` | no | Should waiver info be included. |
| `include_multiple_waivers` | query | `string` | no | Should info for multiple waivers be included? |
| `include_usat_waiver_info` | query | `string` | no | Should USAT waiver info be included. |
| `include_pending_lottery_selection` | query | `string` | no | Should pending lottery selection participants be included. |
| `exclude_registrations_via_super_event` | query | `string` | no | Exclude event registrations that are due to the registrant signing up for a super event that includes this event. |
| `include_shipping_address` | query | `string` | no | Should shipping address be included (if enabled). |
| `include_profile_type` | query | `string` | no | Should profile type be included. |
| `include_profile_image_url` | query | `string` | no | Should profile image URLs be included. |
| `supports_nb` | query | `string` | no | Does integration support non-binary X gender? |
| `include_fundraisers` | query | `string` | no | Should fundraiser and team fundraiser information be included? |
| `include_multi_race_bundle_info` | query | `string` | no | Should multi-race bundle information be included? |
| `include_transferred_participants` | query | `string` | no | Should transferred participants be included? |
| `search_first_name` | query | `string` | no | Search for users by first name. |
| `search_last_name` | query | `string` | no | Search for users by last name. |
| `search_email` | query | `string` | no | Search for users by email address. |
| `search_bib` | query | `number` | no | Search for users by bib number. |
