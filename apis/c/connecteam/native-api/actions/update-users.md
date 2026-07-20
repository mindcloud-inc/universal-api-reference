# Update Users with Connecteam

Update individual or multiple users associated with the account using the provided details. You can specify updates either by their phone number or unique userID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/v1/users`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Update Users](https://developer.connecteam.com/reference/edit_users_users_v1_users_put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `editUsersByPhone` | query | `boolean` | no |
| `includeSmartGroupIds` | query | `boolean` | no |
| `users[]` | body | `array<object>` | no |
| `users[].firstName` | body | `string` | no |
| `users[].lastName` | body | `string` | no |
| `users[].phoneNumber` | body | `string` | no |
| `users[].userType` | body | `string` | no |
| `users[].email` | body | `string` | no |
| `users[].customFields[]` | body | `array<object>` | no |
| `users[].customFields[].customFieldId` | body | `number` | no |
| `users[].customFields[].value` | body | `string` | no |
| `users[].isArchived` | body | `boolean` | no |
| `users[].userId` | body | `number` | yes |
