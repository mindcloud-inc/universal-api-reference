# Update Contact with Loops

Updates or creates a contact in Loops.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/update`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Update Contact](https://loops.so/docs/api-reference/update-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `userId` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `subscribed` | body | `boolean` | no |
| `userGroup` | body | `string` | no |
| `mailingLists` | body | `object` | no |
