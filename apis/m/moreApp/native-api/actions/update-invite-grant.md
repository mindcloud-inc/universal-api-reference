# Update Invite Grant with MoreApp

Updates an invite's grants in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{id}}/grants`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Invite Grant](https://docs.moreapp.com/docs/developer-docs/180b38f242fc7-add-update-remove-grant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `roleId` | body | `string` | no |
| `id` | path | `string` | yes |
| `operation` | body | `string` | yes |
| `resourceId` | body | `string` | yes |
| `resourceType` | body | `string` | yes |
