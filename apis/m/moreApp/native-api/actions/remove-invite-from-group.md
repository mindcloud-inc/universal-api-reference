# Remove Invite From Group with MoreApp

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{inviteId}}/groups/{{groupId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Remove Invite From Group](https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `inviteId` | path | `string` | yes |
| `groupId` | path | `string` | yes |
