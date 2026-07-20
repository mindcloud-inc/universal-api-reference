# Update branch with Neon

Updates a branch in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update branch](https://api-docs.neon.tech/reference/updateprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `branch` | body | `object` | yes | Neon API parameter branch |
