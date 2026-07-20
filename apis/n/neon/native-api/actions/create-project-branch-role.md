# Create role with Neon

Creates a role in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/roles`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create role](https://api-docs.neon.tech/reference/createprojectbranchrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `role` | body | `object` | yes | Neon API parameter role |
