# Create Contact with Superchat

Creates a new contact in Superchat.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Create Contact](https://developers.superchat.com/reference/createcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | The first name of the contact |
| `last_name` | body | `string` | no | The last name of the contact |
| `gender` | body | `string` | no | The gender of the contact |
| `handles[]` | body | `array<object>` | yes | The contact handles associated with this contact |
| `custom_attributes[]` | body | `array<object>` | no | The contact attributes of this contact |
