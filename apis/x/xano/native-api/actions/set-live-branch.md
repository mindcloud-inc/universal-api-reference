# Set Live Branch with Xano

Sets a branch as live in Xano.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch/:branch_label/live`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Set Live Branch](https://docs.xano.com/xano-features/metadata-api/instance_api/set_a_branch_as_the_live_active_branch_for_the_workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch_label` | path | `string` | yes |
| `workspace_id` | path | `number` | yes |
