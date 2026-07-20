# Untag Contact with Cakemail

Removes tags from a contact in Cakemail.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/contacts/:contactId/untag`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Untag Contact](https://cakemail.dev/en/api/contact#untags-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
| `tags[]` | body | `array<string>` | yes | Tags to remove from the contact. |
