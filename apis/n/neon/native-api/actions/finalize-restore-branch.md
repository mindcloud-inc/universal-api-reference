# Finalize restore with Neon

Finalizes branch restore from snapshot in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/finalize_restore`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Finalize restore](https://api-docs.neon.tech/reference/finalizerestorebranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `name` | body | `string` | no | Neon API parameter name |
