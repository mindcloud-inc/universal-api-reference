# Create Contact with OnePageCRM

Creates a new contact in OnePageCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Create Contact](https://developer.onepagecrm.com/api/#/Contacts/post_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | First name of the contact. |
| `last_name` | body | `string` | no | Last name of the contact. |
| `company_name` | body | `string` | no | Name of the company the contact belongs to. |
| `emails[]` | body | `array<object>` | no | Email addresses associated with the contact. |
| `phones[]` | body | `array<object>` | no | Phone numbers associated with the contact. |
| `job_title` | body | `string` | no | Job title of the contact. |
| `title` | body | `string` | no | The title of the contact. |
| `company_id` | body | `string` | no | ID of the company the contact belongs to. |
| `status_id` | body | `list<string>` | no | ID of the contact status. |
| `lead_source_id` | body | `list<string>` | no | ID of the lead source. |
| `owner_id` | body | `list<string>` | no | ID of the user who owns the contact. |
| `tags[]` | body | `array<string>` | no | Tags applied to the contact. |
| `starred` | body | `boolean` | no | Whether the contact is starred. |
| `background` | body | `string` | no | Background information about the contact. |
| `urls[]` | body | `array<object>` | no | URLs associated with the contact. |
| `address_list[]` | body | `array<object>` | no | Addresses associated with the contact. |
| `custom_fields[]` | body | `array<object>` | no | Extra user-configurable contact fields. |
