# Update Contact with Freshdesk

Updates an existing contact in Freshdesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Update Contact](https://developers.freshdesk.com/api/#update_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk contact ID. |
| `name` | body | `string` | no | Name of the contact |
| `email` | body | `string` | no | Primary email address of the contact |
| `phone` | body | `string` | no | Telephone number of the contact |
| `mobile` | body | `string` | no | Mobile number of the contact |
| `twitter_id` | body | `string` | no | Twitter handle of the contact |
| `social_handler[]` | body | `array<object>` | no | Social handles for the contact |
| `unique_external_id` | body | `string` | no | External ID of the contact |
| `other_emails[]` | body | `array<string>` | no | Additional emails associated with the contact |
| `company_id` | body | `list<number>` | no | Primary company ID for the contact |
| `view_all_tickets` | body | `boolean` | no | Whether contact can view all company tickets |
| `other_companies[]` | body | `array<object>` | no | Additional companies associated with the contact |
| `address` | body | `string` | no | Address of the contact |
| `avatar` | body | `file` | no | Avatar image of the contact |
| `custom_fields` | body | `object` | no | Key-value pairs for custom contact fields |
| `description` | body | `string` | no | Short description of the contact |
| `job_title` | body | `string` | no | Job title of the contact |
| `language` | body | `string` | no | Language of the contact |
| `tags[]` | body | `array<string>` | no | Tags associated with the contact |
| `time_zone` | body | `string` | no | Time zone of the contact |
| `lookup_parameter` | body | `string` | no | Lookup field value for custom object linkage |
