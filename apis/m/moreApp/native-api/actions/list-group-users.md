# List Group Users with MoreApp

Retrieves users in a MoreApp group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}/users`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Group Users](https://docs.moreapp.com/docs/developer-docs/af4728fa7f56c-list-users-within-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `groupId` | path | `string` | yes |
