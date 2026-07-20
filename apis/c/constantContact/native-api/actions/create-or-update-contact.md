# Create or Update Contact with Constant Contact

Creates or updates a contact in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/sign_up_form`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create or Update Contact](https://developer.constantcontact.com/api_guide/contacts_create_or_update.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | no | Email address used to create or update the contact. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone_number` | body | `string` | no | SMS-capable phone number for signup flows. |
| `list_memberships[]` | body | `array<string>` | yes | List memberships required by sign-up form endpoint (array of list IDs). |
