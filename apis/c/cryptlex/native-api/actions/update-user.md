# Update User with Cryptlex

Updates an existing user in Cryptlex.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/users/:id`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Update User](https://api.cryptlex.com/v3/docs#tag/Users/operation/patch/v3/users/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the user. |
| `email` | body | `string` | no | Email address for the user. |
| `firstName` | body | `string` | no | First name for the user. |
| `lastName` | body | `string` | no | Last name for the user. |
| `company` | body | `string` | no | Company name for the user. |
| `role` | body | `string` | no | Role assigned to the user. |
| `allowCustomerPortalAccess` | body | `boolean` | no | Whether the user can access the customer portal. |
| `tags` | body | `list<string>` | no | Tags to attach to the user. |
