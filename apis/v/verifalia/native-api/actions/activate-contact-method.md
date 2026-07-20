# Activate Contact Method with Verifalia

Activates a contact method in Verifalia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{user-id}/contact-methods/{contact-method-id}/activation`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Activate Contact Method](https://verifalia.com/developers/users/contact-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The Verifalia user ID. |
| `contact-method-id` | path | `string` | yes | The Verifalia contact method ID. |
| `code` | body | `string` | yes | The activation code Verifalia sent to the contact method. |
