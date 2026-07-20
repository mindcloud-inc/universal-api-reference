# Delete branch with Neon

Deletes a branch from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete branch](https://api-docs.neon.tech/reference/deleteprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
