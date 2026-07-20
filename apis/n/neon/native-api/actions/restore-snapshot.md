# Restore snapshot with Neon

Restores snapshot in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/snapshots/:snapshot_id/restore`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Restore snapshot](https://api-docs.neon.tech/reference/restoresnapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Neon API parameter name |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `snapshot_id` | path | `string` | yes | Neon API parameter snapshot_id |
| `name` | query | `string` | no | Neon API parameter name |
| `target_branch_id` | body | `string` | no | Neon API parameter target_branch_id |
| `finalize_restore` | body | `boolean` | no | Neon API parameter finalize_restore |
