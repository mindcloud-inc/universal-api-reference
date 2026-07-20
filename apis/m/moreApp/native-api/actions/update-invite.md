# Update Invite with MoreApp

Updates an invite in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{id}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Invite](https://docs.moreapp.com/docs/developer-docs/3da3bf74dfc23-update-invite)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `id` | path | `string` | yes |
| `language` | body | `string` | yes |
| `receiveNewsLetter` | body | `boolean` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
