# Create Contact with EmailOctopus

Creates a contact in an EmailOctopus list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/contacts`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Create Contact](https://emailoctopus.com/api-documentation/lists/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | yes | The contact email address. |
| `fields` | body | `object` | no | Custom field values for the contact. |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `status` | body | `string` | no | The subscription status for the contact. |
| `tags[]` | body | `array<string>` | no | Tags to apply to the contact. |
