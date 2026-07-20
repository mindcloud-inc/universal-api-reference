# Delete Contact with Loops

Deletes a contact from Loops by email or user ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/delete`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Delete Contact](https://loops.so/docs/api-reference/delete-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `userId` | body | `string` | no |
