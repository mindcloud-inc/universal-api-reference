# Unsubscribe Contact with Cakemail

Unsubscribes a contact from a Cakemail list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/contacts/:contactId/unsubscribe`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Unsubscribe Contact](https://cakemail.dev/en/api/contact#unsubscribe-a-contact-from-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
