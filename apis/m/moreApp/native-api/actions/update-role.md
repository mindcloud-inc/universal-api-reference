# Update Role with MoreApp

Updates a role in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/customers/{{customerId}}/roles/{{roleId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Role](https://docs.moreapp.com/docs/developer-docs/2bda39e46b7a6-modify-role)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `roleId` | path | `string` | yes |
| `name` | body | `string` | no |
