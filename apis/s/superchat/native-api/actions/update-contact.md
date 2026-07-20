# Update Contact with Superchat

Updates an existing contact in Superchat.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{contact_id}`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Update Contact](https://developers.superchat.com/reference/updatecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact |
| `first_name` | body | `string` | no | The first name of the contact |
| `last_name` | body | `string` | no | The last name of the contact |
| `gender` | body | `string` | no | The gender of the contact |
| `handles[]` | body | `array<object>` | no | The contact handles associated with this contact. Only supported for phone and email handles. |
| `custom_attributes[]` | body | `array<object>` | no | The contact attributes of this contact |
