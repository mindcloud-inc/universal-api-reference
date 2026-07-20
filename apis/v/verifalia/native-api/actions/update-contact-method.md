# Update Contact Method with Verifalia

Updates an existing contact method in Verifalia.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/{user-id}/contact-methods/{contact-method-id}`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Update Contact Method](https://verifalia.com/developers/users/contact-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The Verifalia user ID. |
| `contact-method-id` | path | `string` | yes | The Verifalia contact method ID. |
