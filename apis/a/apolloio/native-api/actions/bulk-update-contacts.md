# Bulk Update Contacts with Apollo

Updates multiple existing contacts in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/contacts/bulk_update`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Bulk Update Contacts](https://docs.apollo.io/reference/bulk-update-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids[]` | body | `array<string>` | no | Array of contact IDs to update with the same values. Use this for applying the same updates to multiple contacts. |
| `contact_attributes[]` | body | `array<object>` | no | Array of contact objects with individual updates. Use this for applying different updates to each contact. |
| `contact_attributes[].id` | body | `string` | yes | The contact ID to update |
| `contact_attributes[].first_name` | body | `string` | no | The contact's first name |
| `contact_attributes[].last_name` | body | `string` | no | The contact's last name |
| `contact_attributes[].email` | body | `string` | no | The contact's email address |
| `contact_attributes[].title` | body | `string` | no | The contact's job title |
| `contact_attributes[].organization_name` | body | `string` | no | The contact's organization name |
| `contact_attributes[].owner_id` | body | `string` | no | The Apollo user ID to assign as owner |
| `contact_attributes[].account_id` | body | `string` | no | The Apollo account ID to associate with the contact |
| `contact_attributes[].present_raw_address` | body | `string` | no | The contact's location |
| `contact_attributes[].linkedin_url` | body | `string` | no | The contact's LinkedIn profile URL |
| `contact_attributes[].typed_custom_fields` | body | `object` | no | Custom field values as key-value pairs |
| `owner_id` | body | `string` | no | When using contact_ids, apply this owner to all contacts |
| `email` | body | `string` | no | When using contact_ids, apply this email to all contacts |
| `organization_name` | body | `string` | no | When using contact_ids, apply this organization name to all contacts |
| `title` | body | `string` | no | When using contact_ids, apply this title to all contacts |
| `first_name` | body | `string` | no | When using contact_ids, apply this first name to all contacts |
| `last_name` | body | `string` | no | When using contact_ids, apply this last name to all contacts |
| `account_id` | body | `string` | no | When using contact_ids, apply this account ID to all contacts |
| `present_raw_address` | body | `string` | no | When using contact_ids, apply this address to all contacts |
| `linkedin_url` | body | `string` | no | When using contact_ids, apply this LinkedIn URL to all contacts |
| `typed_custom_fields` | body | `object` | no | When using contact_ids, apply these custom fields to all contacts |
| `async` | body | `boolean` | no | Force asynchronous processing. Automatically enabled for >100 contacts. |
| `visible_entity_ids[]` | body | `array<string>` | no | Specific contact IDs to return in the response (for performance) |
