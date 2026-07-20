# Create Contact with Constant Contact

Creates a contact in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create Contact](https://developer.constantcontact.com/api_guide/contacts_post_one.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address.address` | body | `string` | yes | Primary email address for the contact (must be unique in Constant Contact). |
| `email_address.permission_to_send` | body | `string` | yes | Permission level for sending email to this contact. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `create_source` | body | `string` | yes | Who created the contact (required for compliance). Accepted values: `0`, `1`. |
| `list_memberships[]` | body | `array<string>` | no | Optional. Array of list IDs. Do not pass objects; each item must be a list_id string. Accepted values: `0`. Send multiple values as a array. |
