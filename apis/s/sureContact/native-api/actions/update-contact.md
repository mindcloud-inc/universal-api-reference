# Update Contact with SureContact

Updates an existing contact in SureContact.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v1/public/contacts/:contact_uuid`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Update Contact](https://api.surecontact.com/docs#contact-management-PUTapi-v1-public-contacts--contact_uuid-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuid` | path | `string` | yes | The UUID of the contact. |
| `custom_fields` | body | `object` | no | Custom field values keyed by field name. |
| `metadata` | body | `object` | no | Additional metadata as key-value pairs. |
| `primary_fields` | body | `object` | no | Primary contact information. |
| `primary_fields.company` | body | `string` | no | The contact company name. |
| `primary_fields.email` | body | `string` | no | The contact email address. |
| `primary_fields.first_name` | body | `string` | no | The contact first name. |
| `primary_fields.job_title` | body | `string` | no | The contact job title. |
| `primary_fields.last_name` | body | `string` | no | The contact last name. |
| `primary_fields.phone` | body | `string` | no | The contact phone number. |
| `primary_fields.status` | body | `string` | no | The contact status. |
