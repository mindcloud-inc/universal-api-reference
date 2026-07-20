# Set Permission Roles with Frontegg

Updates the roles assigned to a permission in Frontegg.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/resources/permissions/v1/:permissionId/roles`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Set Permission Roles](https://developers.frontegg.com/ciam/api/identity/permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permissionId` | path | `string` | yes | Permission ID. |
| `roleIds[]` | body | `array<string>` | yes | Role IDs to assign. |
