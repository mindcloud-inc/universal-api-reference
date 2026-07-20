# Get Contact with Cakemail

Retrieves a contact from a Cakemail list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/contacts/:contactId`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Get Contact](https://cakemail.dev/en/api/contact#show-a-contact-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
