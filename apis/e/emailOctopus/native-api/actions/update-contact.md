# Update Contact with EmailOctopus

Updates a contact in an EmailOctopus list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId/contacts/:memberId`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Update Contact](https://emailoctopus.com/api-documentation/lists/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | no | The updated contact email address. |
| `fields` | body | `object` | no | Custom field values for the contact. |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `memberId` | path | `string` | yes | The unique ID of the contact. |
| `status` | body | `string` | no | The subscription status for the contact. |
| `tags[]` | body | `array<string>` | no | Tags to apply to the contact. |
