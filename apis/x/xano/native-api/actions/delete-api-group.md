# Delete API Group with Xano

Deletes an existing API group from Xano.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Delete API Group](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_an_api_group_and_all_its_endpoints_this_action_cannot_be_undone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
