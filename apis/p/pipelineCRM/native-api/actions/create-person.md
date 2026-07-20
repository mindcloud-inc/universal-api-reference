# Create Person with Pipeline CRM

Creates a new person in Pipeline CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/people`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [Create Person](https://app.pipelinecrm.com/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliver_reassignment_email` | query | `boolean` | no | Send an assignment email when the person is assigned to another user. |
| `person.first_name` | body | `string` | no | The person's first name. |
| `person.last_name` | body | `string` | no | The person's last name. |
| `person.full_name` | body | `string` | no | The person's full name. |
| `person.summary` | body | `string` | no | Summary or notes on the person. |
| `person.phone` | body | `string` | no | Person's primary phone number. |
| `person.mobile` | body | `string` | no | Person's mobile phone number. |
| `person.position` | body | `string` | no | Person's professional position. |
| `person.website` | body | `string` | no | Person's website URL. |
| `person.email` | body | `string` | no | Person's primary email address. |
| `person.company_id` | body | `number` | no | The company ID associated with this person. |
| `person.company_name` | body | `string` | no | Associates a company to this person by name, creating it if needed. |
| `person.user_id` | body | `number` | no | The user ID who owns this person record. |
| `person.lead_status_id` | body | `number` | no | The lead status ID to set for this person. |
| `person.lead_source_id` | body | `number` | no | The lead source ID to set for this person. |
| `person.predefined_contacts_tag_ids[]` | body | `array<number>` | no | Tag IDs to set on this person. |
| `person.relationship` | body | `string` | no | The relationship of the person to the company. |
| `person.is_key_contact` | body | `boolean` | no | Whether this person is a key contact for the company. |
| `todo_template_id` | body | `number` | no | The todo template ID to apply to this person. |
| `todo_template_user_id` | body | `number` | no | The owner of tasks created from the todo template. |
