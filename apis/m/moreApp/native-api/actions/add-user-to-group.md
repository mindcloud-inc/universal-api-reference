# Add User To Group with MoreApp

Adds a user to a group in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}/users/{{userId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Add User To Group](https://docs.moreapp.com/docs/developer-docs/81d814eeaa125-add-user-to-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `groupId` | path | `string` | yes |
| `userId` | path | `string` | yes |
