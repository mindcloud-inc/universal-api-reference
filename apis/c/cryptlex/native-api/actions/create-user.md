# Create User with Cryptlex

Creates a user in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/users`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create User](https://api.cryptlex.com/v3/docs#tag/Users/operation/post/v3/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the user. |
| `firstName` | body | `string` | yes | First name for the user. |
| `password` | body | `string` | yes | Password for the user. |
| `lastName` | body | `string` | no | Last name for the user. |
| `company` | body | `string` | no | Company name for the user. |
| `role` | body | `string` | yes | Role assigned to the user. |
| `allowCustomerPortalAccess` | body | `boolean` | no | Whether the user can access the customer portal. |
| `tags[]` | body | `array<string>` | no | Tags to attach to the user. |
