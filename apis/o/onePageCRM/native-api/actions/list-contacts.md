# List Contacts with OnePageCRM

Retrieves contacts from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Contacts](https://developer.onepagecrm.com/api/#/Contacts/get_contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `boolean` | no | Include contacts owned by other users. |
| `search` | query | `string` | no | Search contacts by contact name, company name, or phone number. |
| `phone` | query | `string` | no | Search contacts by phone number. |
| `url` | query | `string` | no | Search contacts by web address. |
| `action_stream` | query | `boolean` | no | Only return results that are also in the action stream. |
| `has_actions` | query | `boolean` | no | Only return contacts owned by the logged user that have actions for any user. |
| `has_actions_for_me` | query | `boolean` | no | Only return contacts owned by the logged user that have actions for the logged user. |
| `has_actions_today` | query | `boolean` | no | Only return contacts owned by the logged user that have actions today for the logged user. |
| `pending_deal` | query | `boolean` | no | Only return contacts who have a pending deal. |
| `starred` | query | `boolean` | no | Only return contacts who are starred. |
| `waiting` | query | `boolean` | no | Only return contacts, for whom the logged user has a next action, of status waiting. |
| `email` | query | `string` | no | Return contacts whose email matches the provided value. |
| `letter` | query | `string` | no | Return contacts whose last name begins with the specified letter. |
| `custom_field_id` | query | `string` | no | Filter contacts by custom field value. Use with Custom Field Value. |
| `custom_field_value` | query | `string` | no | Filter contacts by custom field value. Use with Custom Field ID. |
| `lead_source` | query | `string` | no | Return contacts of a specific lead source. Use either Lead Source or Lead Source ID. |
| `lead_source_id` | query | `list<string>` | no | Return contacts of a specific lead source. Use either Lead Source or Lead Source ID. |
| `status_id` | query | `list<string>` | no | Return contacts of a particular status. |
| `not_linked_with` | query | `string` | no | Only return contacts who are not linked to a particular company ID. |
| `owner_id` | query | `list<string>` | no | Return contacts owned by a specific user. |
| `company_id` | query | `string` | no | Return contacts from a specific company. Use only one of Company ID, Tag, or Filter ID. |
| `tag` | query | `string` | no | Filter contacts by tag. Use only one of Company ID, Tag, or Filter ID. |
| `filter_id` | query | `string` | no | Apply a filter to contact listing. Use only one of Company ID, Tag, or Filter ID. |
| `date_filter` | query | `list<string>` | no | Choose which date field to use with Since and Until. Accepted values: `created_at`, `modified_at`, `updated_at`. |
| `since` | query | `date` | no | Start of the date range to filter resources that were added or edited. |
| `until` | query | `date` | no | End of the date range to filter resources that were added or edited. |
| `modified_since` | query | `date` | no | Return only resources that were modified since the specified time. |
| `unmodified_since` | query | `date` | no | Return only resources that were unmodified since the specified time. |
