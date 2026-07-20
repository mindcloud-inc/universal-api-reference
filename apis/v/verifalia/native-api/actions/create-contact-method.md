# Create Contact Method with Verifalia

Creates a new contact method in Verifalia.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{user-id}/contact-methods`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Create Contact Method](https://verifalia.com/developers/users/contact-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The Verifalia user ID. |
| `type` | body | `string` | yes | The contact method type. Verifalia currently supports only `Email`. |
| `displayName` | body | `string` | yes | A user-friendly label for the contact method. |
| `emailAddress` | body | `string` | yes | The email address to bind as a contact method. |
