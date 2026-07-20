# Create Contact with 2Chat

Creates a new contact in 2Chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Create Contact](https://developers.2chat.co/docs/API/Contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | — |
| `last_name` | body | `string` | no | — |
| `profile_pic_url` | body | `string` | no | — |
| `channel_uuid` | body | `string` | no | Assign the contact to a specific WhatsApp channel UUID. |
| `contact_detail[]` | body | `array<object>` | yes | Provide at least one contact method such as a phone number or email address. |
| `type` | body | `string` | yes | — |
| `value` | body | `string` | yes | — |
| `custom_field[]` | body | `array<object>` | no | Optional custom field entries stored on the contact. |
| `title` | body | `string` | no | — |
| `value` | body | `string` | no | — |
