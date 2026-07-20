# Create Contact with Marketing Master IO

Creates a new contact in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/list`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Create Contact](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id[]` | body | `array<string>` | no | Array of contact book IDs to add the contact to. Send multiple values as a array. |
| `email` | body | `string` | no | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `phone_number` | body | `string` | no | — |
| `subscriber` | body | `boolean` | yes | Set true to subscribe the contact or false to unsubscribe. |
| `tag[]` | body | `array<string>` | no | Array of tag IDs to apply to the contact. Send multiple values as a array. |
