# Remove Contact Suppression with Loops

Deletes contact suppression from Loops by email or user ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/suppression`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Remove Contact Suppression](https://loops.so/docs/api-reference/remove-contact-suppression)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | no |
| `userId` | query | `string` | no |
