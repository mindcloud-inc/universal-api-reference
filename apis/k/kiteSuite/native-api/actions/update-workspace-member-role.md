# Update Workspace Member Role with KiteSuite

Updates a workspace member role in KiteSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace/member/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Workspace Member Role](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Runtime expects the user ID for the workspace member. |
| `roleID` | body | `string` | yes | Workspace role ID to assign. |
