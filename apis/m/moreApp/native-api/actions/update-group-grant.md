# Update Group Grant with MoreApp

Updates a group's grants in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}/grants`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Group Grant](https://docs.moreapp.com/docs/developer-docs/9f16580180528-add-remove-grant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `roleId` | body | `string` | no |
| `groupId` | path | `string` | yes |
| `operation` | body | `string` | yes |
| `resourceId` | body | `string` | yes |
| `resourceType` | body | `string` | yes |
