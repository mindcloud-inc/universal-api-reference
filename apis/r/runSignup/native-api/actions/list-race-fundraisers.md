# List Race Fundraisers with RunSignup

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/race-fundraisers/get-race-fundraisers.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [List Race Fundraisers](https://runsignup.com/API/v2/race-fundraisers/get-race-fundraisers.json/GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | ID of race. |
| `donation_period_id` | query | `number` | no | Get fundraisers associated with a donation period ID. |
| `num` | query | `number` | no | Number of results per page. The allowed range per page is from 1 - 500, outside this range it defaults to 50 per page. |
| `page` | query | `number` | no | Number of pages. |
| `modified_after_ts` | query | `number` | no | Get fundraisers updated after the provided timestamp. |
| `modified_before_ts` | query | `number` | no | Get fundraisers updated before the provided timestamp. |
| `include_amount_raised` | query | `string` | no | Get amount raised for fundraisers? |
| `modified_field` | query | `string` | no | Consider only metadata changes or metadata and donation amount changes? Allowed values are 'meta' or 'meta_or_donation'. |
| `include_number_of_donations` | query | `string` | no | Include number of donations. |
| `include_fundraiser_profile_images` | query | `string` | no | Include fundraiser profile image. |
| `included_fundraiser_types` | query | `string` | no | Include fundraisers types. Allowed values: 'any', 'individuals', 'teams' |
| `include_fundraiser_type_info` | query | `string` | no | Include team fundraiser type info. |
| `include_umbrella_teams` | query | `string` | no | Include umbrella team info. |
| `include_import_data` | query | `string` | no | (Deprecated: Use `include_external_fundraiser_ids` instead.) Include external fundraiser info. |
| `include_external_fundraiser_ids` | query | `string` | no | Include external fundraiser info. |
| `include_minimum_commitment_data` | query | `string` | no | Include minimum commitment info. |
| `registration_id` | query | `number` | no | Get fundraiser associated with a registration ID. |
| `fundraiser_id` | query | `number` | no | Get fundraiser associated with a fundraiser ID. |
| `after_fundraiser_id` | query | `number` | no | Get fundraisers with IDs greater than specified fundraiser ID. |
| `sort` | query | `string` | no | Sort by “created_ts”, “last_modified_ts”, “race_fundraiser_id”, or “amount_raised”. |
| `sort_direction` | query | `string` | no | Sort direction. Only applicable if `sort` is specified. |
