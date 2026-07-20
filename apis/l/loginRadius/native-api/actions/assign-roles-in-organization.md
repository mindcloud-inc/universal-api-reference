# Assign Roles in Organization with LoginRadius

Updates a user's organization roles in LoginRadius.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/manage/account/:uid/orgcontext/:orgId/roles`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Assign Roles in Organization](https://www.loginradius.com/docs/api/openapi/assign-roles-to-user/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Organization ID in which to assign roles. |
| `roleId` | body | `string` | yes | Role ID to assign within the organization. |
| `uid` | path | `string` | yes | UID of the user to assign roles to. |
