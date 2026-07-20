# Update Project Member Role with KiteSuite

Updates a project member role in KiteSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/project/member/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Project Member Role](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Runtime expects the user ID for the project member. |
| `projectID` | body | `string` | yes | Project ID. |
| `roleID` | body | `string` | yes | Project role ID to assign. |
