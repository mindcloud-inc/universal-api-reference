# Update Contact with 2Chat

Updates an existing contact in 2Chat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactUuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Update Contact](https://developers.2chat.co/docs/API/Contacts/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactUuid` | path | `string` | yes | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `profile_pic_url` | body | `string` | no | — |
| `channel_uuid` | body | `string` | no | Move the contact to a specific WhatsApp channel UUID. |
