# Update Contact with Cakemail

Updates an existing contact in a Cakemail list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/lists/:listId/contacts/:contactId`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Update Contact](https://cakemail.dev/en/api/contact#update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
| `email` | body | `string<string>` | no | Updated email address for the contact. |
| `tags[]` | body | `array<string>` | no | Tags to set on the contact. |
