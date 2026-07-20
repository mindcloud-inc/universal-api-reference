# List Action Stream Contacts with OnePageCRM

Retrieves contacts from OnePageCRM prioritized by next action.

## Endpoint

- **Method:** `GET`
- **Path:** `/action_stream`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Action Stream Contacts](https://developer.onepagecrm.com/api/#/Action_Stream/get_action_stream)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search contacts by contact name, company name, or phone number. |
| `email` | query | `string` | no | Match contacts by email address. |
| `phone` | query | `string` | no | Search contacts by phone number. |
| `url` | query | `string` | no | Search contacts by web address. |
| `team` | query | `boolean` | no | Include contacts owned by other users. |
| `letter` | query | `string` | no | Match contacts whose last name begins with the specified letter. |
| `status_id` | query | `string` | no | Return contacts of a particular status. |
| `owner_id` | query | `string` | no | Return contacts owned by a specific user. |
| `company_id` | query | `string` | no | Return contacts from a specific company. |
| `tag` | query | `string` | no | Filter contacts by tag. |
| `filter_id` | query | `string` | no | Apply a saved contact filter. |
| `lead_source` | query | `string` | no | Return contacts of a specific lead source. |
| `lead_source_id` | query | `string` | no | Return contacts of a specific lead source by ID. |
| `custom_field_id` | query | `string` | no | Custom field ID to combine with Custom Field Value. |
| `custom_field_value` | query | `string` | no | Custom field value to combine with Custom Field ID. |
| `action_stream` | query | `boolean` | no | Only return results that are also in the action stream. |
| `has_actions` | query | `boolean` | no | Return owned contacts that have actions for any user. |
| `has_actions_for_me` | query | `boolean` | no | Return owned contacts that have actions for the logged user. |
| `pending_deal` | query | `boolean` | no | Only return contacts that have a pending deal. |
| `starred` | query | `boolean` | no | Only return starred contacts. |
| `waiting` | query | `boolean` | no | Only return contacts where my next action has waiting status. |
| `date_filter` | query | `list<string>` | no | Choose which date field to use with Since or Until. Accepted values: `created_at`, `modified_at`, `updated_at`. |
| `since` | query | `date` | no | Return resources added or edited since this date or timestamp. |
| `until` | query | `date` | no | Return resources added or edited until this date or timestamp. |
| `modified_since` | query | `date` | no | Return only resources modified since this date or timestamp. |
| `unmodified_since` | query | `date` | no | Return only resources unmodified since this date or timestamp. |
