# Tag Contact with Cakemail

Updates tags on a contact in Cakemail.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/contacts/:contactId/tag`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Tag Contact](https://cakemail.dev/en/api/contact#tags-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
| `tags[]` | body | `array<string>` | yes | Tags to apply to the contact. |
