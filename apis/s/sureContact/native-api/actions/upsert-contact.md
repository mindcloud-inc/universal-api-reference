# Upsert Contact with SureContact

Creates or updates a contact in SureContact by email.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/contacts/upsert`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Upsert Contact](https://api.surecontact.com/docs#contact-management-POSTapi-v1-public-contacts-upsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_fields` | body | `object` | no | Custom field values keyed by field name. |
| `list_uuids[]` | body | `array<string>` | no | Static list UUIDs to attach to the contact. |
| `metadata` | body | `object` | no | Additional metadata as key-value pairs. |
| `primary_fields` | body | `object` | yes | Primary contact information. |
| `primary_fields.company` | body | `string` | no | The contact company name. |
| `primary_fields.email` | body | `string` | yes | The contact email used for upsert matching. |
| `primary_fields.first_name` | body | `string` | no | The contact first name. |
| `primary_fields.job_title` | body | `string` | no | The contact job title. |
| `primary_fields.last_name` | body | `string` | no | The contact last name. |
| `primary_fields.phone` | body | `string` | no | The contact phone number. |
| `primary_fields.status` | body | `string` | no | The contact status. |
| `tag_uuids[]` | body | `array<string>` | no | Tag UUIDs to attach to the contact. |
