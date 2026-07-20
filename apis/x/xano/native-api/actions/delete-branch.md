# Delete Branch with Xano

Deletes an existing branch from Xano.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch/:branch_label`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Delete Branch](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_a_workspace_branch_cannot_delete_the_default_branch_or_currently_live_branch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch_label` | path | `string` | yes |
| `workspace_id` | path | `number` | yes |
