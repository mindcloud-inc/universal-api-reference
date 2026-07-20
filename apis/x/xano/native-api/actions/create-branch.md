# Create Branch with Xano

Creates a new branch in a Xano workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Create Branch](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_branch_by_cloning_an_existing_branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Branch label. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
