# Remove User with MoreApp

Removes a user from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/customers/{{customerId}}/users/{{userId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Remove User](https://docs.moreapp.com/docs/developer-docs/c6474802fa5c1-remove-a-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `userId` | path | `string` | yes |
