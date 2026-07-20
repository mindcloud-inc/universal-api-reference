# Get User Grants with MoreApp

Retrieves a user's grants from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers/{{customerId}}/users/{{userId}}/grants`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Get User Grants](https://docs.moreapp.com/docs/developer-docs/3bd1645996df5-get-grants-for-user)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `userId` | path | `string` | yes |
