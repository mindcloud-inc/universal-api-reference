# Update Permission with Frontegg

Updates an existing permission in Frontegg.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/identity/resources/permissions/v1/:permissionId`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update Permission](https://developers.frontegg.com/ciam/api/identity/permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permissionId` | path | `string` | yes | Permission ID. |
| `key` | body | `string` | no | Updated permission key. |
| `name` | body | `string` | no | Updated permission name. |
| `description` | body | `string` | no | Updated permission description. |
| `categoryId` | body | `string` | no | Updated permission category ID. |
