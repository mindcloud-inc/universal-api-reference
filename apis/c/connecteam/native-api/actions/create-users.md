# Create Users with Connecteam

Create individual or multiple users associated with the account using the provided details.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/v1/users`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Create Users](https://developer.connecteam.com/reference/create_users_users_v1_users_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sendActivation` | query | `boolean` | no |
| `users[]` | body | `array<object>` | no |
| `users[].firstName` | body | `string` | yes |
| `users[].lastName` | body | `string` | yes |
| `users[].phoneNumber` | body | `string` | yes |
| `users[].userType` | body | `string` | yes |
| `users[].email` | body | `string` | no |
| `users[].customFields[]` | body | `array<object>` | no |
| `users[].customFields[].customFieldId` | body | `number` | no |
| `users[].customFields[].value` | body | `string` | no |
| `users[].isArchived` | body | `boolean` | no |
