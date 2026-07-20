# Add Invite To Group with MoreApp

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{inviteId}}/groups/{{groupId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Add Invite To Group](https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `inviteId` | path | `string` | yes |
| `groupId` | path | `string` | yes |
