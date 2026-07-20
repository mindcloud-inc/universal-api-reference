# Create Contact with Loops

Creates a new contact in Loops.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/create`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Create Contact](https://loops.so/docs/api-reference/create-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `userId` | body | `string` | no |
| `subscribed` | body | `boolean` | no |
| `userGroup` | body | `string` | no |
| `mailingLists` | body | `object` | no |
| `source` | body | `string` | no |
