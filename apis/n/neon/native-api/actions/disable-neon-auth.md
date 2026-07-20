# Disables Neon Auth for the branch with Neon

Disables Neon Auth for the branch in Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/auth`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Disables Neon Auth for the branch](https://api-docs.neon.tech/reference/disableneonauth)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `delete_data` | body | `boolean` | no | Neon API parameter delete_data |
