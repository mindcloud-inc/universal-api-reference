# Delete Contact Method with Verifalia

Deletes an existing contact method from Verifalia.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/{user-id}/contact-methods/{contact-method-id}`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Delete Contact Method](https://verifalia.com/developers/users/contact-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The Verifalia user ID. |
| `contact-method-id` | path | `string` | yes | The Verifalia contact method ID. |
