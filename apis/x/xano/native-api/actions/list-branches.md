# List Branches with Xano

Finds branches in a Xano workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [List Branches](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_all_branches_in_a_workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
