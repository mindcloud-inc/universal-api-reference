# Update Contact with Constant Contact

Updates a contact in Constant Contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Update Contact](https://developer.constantcontact.com/api_guide/contacts_put.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Unique ID of the contact to update. |
| `update_source` | body | `string` | yes | Source used for this contact update. |
| `email_address.address` | body | `string` | no | Updated primary email address. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
| `list_memberships[]` | body | `array<string>` | no | List IDs to set on update (array of strings). |
