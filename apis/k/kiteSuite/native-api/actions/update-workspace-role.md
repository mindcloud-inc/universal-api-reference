# Update Workspace Role with KiteSuite

Updates an existing workspace role in KiteSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace-role/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Workspace Role](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Workspace role ID. |
| `roleName` | body | `string` | yes | Updated workspace role name. |
