# Update Multiple Contacts with EmailOctopus

Updates multiple contacts in an EmailOctopus list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId/contacts`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Update Multiple Contacts](https://emailoctopus.com/api-documentation/lists/update-contact-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Bulk contact payloads to update. |
| `listId` | path | `string` | yes | The unique ID of the list. |
