# Restore branch with Neon

Restores branch to a historical state in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/restore`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Restore branch](https://api-docs.neon.tech/reference/restoreprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `source_branch_id` | body | `string` | yes | Neon API parameter source_branch_id |
| `source_lsn` | body | `string` | no | Neon API parameter source_lsn |
| `source_timestamp` | body | `date` | no | Neon API parameter source_timestamp |
| `preserve_under_name` | body | `string` | no | Neon API parameter preserve_under_name |
