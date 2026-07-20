# Remove User From Group with MoreApp

Removes a user from a group in MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}/users/{{userId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Remove User From Group](https://docs.moreapp.com/docs/developer-docs/fb988900981f1-remove-user-from-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `groupId` | path | `string` | yes |
| `userId` | path | `string` | yes |
