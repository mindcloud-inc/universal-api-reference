# Get Branch with Xano

Retrieves a branch from Xano by label.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch/:branch_label`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Get Branch](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_specific_branch_by_label)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch_label` | path | `string` | yes |
| `workspace_id` | path | `number` | yes |
