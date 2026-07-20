# Update Contact with Marketing Master IO

Updates an existing contact in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/list/:contact_id`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Update Contact](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id[]` | body | `array<string>` | no | Array of contact book IDs to add the contact to. Send multiple values as a array. |
| `contact_id` | path | `string` | yes | — |
| `subscriber` | body | `boolean` | no | Set true to subscribe the contact or false to unsubscribe. |
| `tag[]` | body | `array<string>` | no | Array of tag IDs to apply to the contact. Send multiple values as a array. |
