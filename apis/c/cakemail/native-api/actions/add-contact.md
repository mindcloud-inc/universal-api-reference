# Add Contact with Cakemail

Creates a new contact in a Cakemail list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/contacts`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Add Contact](https://cakemail.dev/en/api/contact#add-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `email` | body | `string` | yes | Email address for the contact. |
| `send_double_opt_in` | query | `string` | no | Whether and when Cakemail should send a double opt-in confirmation email. |
| `resubscribe` | query | `boolean` | no | Whether to resubscribe the contact when applicable. |
